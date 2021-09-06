# Answer template for Lab 4: Shellcoding

Make a step-by-step report from what you did. (What, why and how?)
You can use screenshots, code snippets and anything, what Markdown enables you to use. 

Answer at least for the questions presented here in each section.
They should be same than in actual instructions, but bit more precise. *If there is confusion, use the instructions repository as it is always up-to-date.*

You can add source files to [src](src) folder and screenshots to [img](img) folder. Source files can be shown alternatively just as code snippets.

You have to create src folder by yourself.

***You can remove questions and just leave task numbers/letters if you want.***

**Answer to this document, and push changes to Git!**

## Task 1 : Basics of buffer overflows

### A) Using program with improper input validation and analyzing overflow

* What is the role of the rip (instruction pointer) register and ret instruction?

* Mention if you used the example program. If you did not, paste the code

    ```c
    into this code snippet
    ```

* What is causing the buffer overflow? (Why it is happening?)

* Provide a screenshot and command of situation, where you managed to reach instruction pointer register, when adding only **one byte** into this register.

    Commands can be shown here like code snippets:
    ```shell
    $ echo $(python -c 'print("This is magic")')
    This is magic
    ```
    Screenshots like this: (add it to img folder, and reference here)

    ![Big overflow](img/placeholder.png "Big overflow" )


### B) Adding hidden (non-used) function to previous program. (And still executing it)

* Show your new function here as code snippet:

    ```c
    my function
    ```


* How did you execute function by just overflowing the input?
  ```shell
  insert command here
  ```
  Describe, what command is containing/actually doing, and how did you find required information for command.



## Task 2 : Arbitrary code execution

### A) Making a simple program to open Shell.

* Paste your C - source file here as code snippet. 

    ```c
    My simple program
    ```

## B) Transforming functionality to machine instructions

* Add source file of your assembly program here as code snippet.
    ```arm
    My assembly program
    ```
* Describe each line(purpose) of assembly code. You can make this by adding comments to source.
* Describe how did you turn your assembly code to shellcode
* Add the results of it by showing shellcode and provide screenshot of situation, where you tested the execution of it, and it worked.

    ```shell
    My shellcode
    ```
    My screenshot:

     ![Big overflow](img/placeholder.png "Big overflow" )

### C) Making the final payload and executing it

How did you find the required information to open shell by overflowing input?

Make a step-by-step report (what, why and how), including command line commands you used to success of executing arbitary code on vulnerable program,by finally opening local shell outside of GDB.
Include a screenshot of the final situation, when you were able to open shell.

## Task 3 : Defeating No-eXecute

### A) Return-to-libc (aka ret2libc)

> ***In this task, you should make example implementation of this ret2libc method. It could be for example spawning local shell. This time, **do not** disable NX protection (do not use -z execstack flag in compiler). Disabling other protections is still required. Like previously, make step by step report(what, why, how) including source files and command line commands which lead you to get shell access.***

 * Describe, how and why did you find possible memory address(es)
 * What is the logic on your payload. (Show it as well)
 * Why it is working?
 * Provide screenshot, when you execute it


### B) Return-oriented programming (aka ROP)

> ***Try to get previously mentioned example (ROP_hello) to work by yourself. Next, make simple example implementation of ROP technique.***

> ***Example: This could be spawning a local shell. To not make it same as ret2libc method, print some text before spawning shell, and print also something after exiting the shell. In this way we can apply some ROP - chain.***

 * Explain, how did you find suitable memory address(es)
   * All the required commands
 * Explain, what your new rop -chain is actually doing.
 * Include new source code to *src* folder
 * Provide screenshot from the execution

## Task 4 : Defeating ASLR (PIE disabled)

Create step-by-step report of how you developed the exploit. This should include:

* How did you read process memory using the vulnerability and how did you restore the process state after read, so it doesn't exit/segfault
* How did you use that information to find memory addresses of libc functions/gadgets that are not in the .got.plt section, required to spawn the shell.
* If you used debugger (e.g., gdb), explain how you used the debugger to debug the exploit.
* Include screenshot of the exploit console output & spawned shell
* Deliver working exploit, put the source code into the *src* folder
* If you run into problems, describe shortly what problems did you have and how you solved them
