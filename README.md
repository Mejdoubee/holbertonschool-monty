# Monty Language Interpreter

This project is a simple Monty language interpreter written in C. Monty is a scripting language that is first compiled into Monty byte codes. It relies on a unique stack, with specific instructions to manipulate it.

## Files and their functions:

1. `monty.h` - Contains all function prototypes, struct definitions, and library includes.

2. `main.c` - The entry point of the program. It opens the bytecode file, reads each line, and passes the opcode to the interpreter.

3. `interpret.c` - Contains the interpreter function which compares the opcode to known instructions and executes the corresponding function.

4. `new_push_pall.c` - Contains the functions for creating a new node, pushing it onto the stack, and printing all elements of the stack.

5. `is_all_digits.c` - Contains a function for checking if a given string contains only digits.

6. `free_stack.c` - Contains a function for Frees a doubly linked.

## Usage:

The Monty language interpreter can be compiled and run with a Monty byte code file as follows:

```bash
$ gcc -Wall -Werror -Wextra -pedantic *.c -o monty
```

```bash
USER@ubuntu:~/monty$ cat -e bytecodes/00.m
push 1$
push 2$
push 3$
pall$
USER@ubuntu:~/monty$ ./monty bytecodes/00.m
3
2
1
USER@ubuntu:~/monty
```


In the `bytecodes/` directory, you'll find some examples of Monty byte code files.

## Note:

This project is still in development and only supports the `push` and `pall` opcodes for the moment. More opcodes will be added in the future. 

## Memory Management:

The program frees all dynamically allocated memory before exiting, ensuring there are no memory leaks.

## Error Handling:

The program has extensive error handling for scenarios such as incorrect usage, inability to open the file, invalid instructions, invalid arguments to instructions, and failures to malloc memory. In such cases, the program exits with the status `EXIT_FAILURE`.

# holbertonschool-monty
