Monty
monty is an interpreter of Monty ByteCodes files which is a scripting language just like Python.

About the Monty language
This is a language that contains specific instructions to manipulate data information (stacks or queues), where each instruction (called opcode) is sended per line. Files which contains Monty byte codes usually have the .m extension.

Example (file.m):

$ cat file.m
# Pushing element to the stack
push 0
push 1
push 2
# Printing all elements
pall
push 3
push 4
pop
# Rotating the stack to the bottom
rotr
pall
rotl
# Setting FIFO
queue
push 5
# Setting LIFO
stack
push 5
$

Technologies
Interpreter was written with C language
C files are compiled using gcc
C files are written according to the betty coding standard
Tested on Ubuntu 20.04 LTS

Usage
To compile all files:

$ gcc -Wall -Werror -Wextra -pedantic *.c -o monty
$
The synopsis of the interpreter is the following:

$ ./monty [filename]
$
To run the interpreter:

$ ./monty file.m
2
1
0
0
3
2
1
$
