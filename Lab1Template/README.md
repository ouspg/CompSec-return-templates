# **Answer template for Computer security lab 2: Fuzzing**

Fill in your answers to this template, answer every question. If screenshots are required, add them to "img" folder. Example of how to add images can be seen at the end of task 2.

If your own code is required, you can paste it to this document or create a "src" folder and add your code there.

## Task 1:
#### Step 1.
Try out Radamsa using command line tool. Print 10 malformed samples of "Fuzztest 1337" using _echo_. 

**Provide the command line you used**
```
answer here
```

#### Step 2.
 What you just did can be done to various types of files too. Next, generate a bunch of .txt test samples for later usage. Create a .txt file, that contains text: "12 EF" and nothing more. Use radamsa to generate 100 fuzzed samples of the file and to name them fuzz1, fuzz2, fuzz3,...etc.

 __Hint__: Create a new, separate folder for the samples.

**Provide the content of 2 different samples that radamsa created**
```

```
**Command line used to create the samples**
```

```

## Task 2:
Your task is to analyze an example c-program *example.c*. Compile the code with appropriate sanitizer flags to enable AddressSanitizer. Run the compiled program and analyze what happens.

**Command line used to compile the program**
```

```
**Screenshot of the result after running the program**
```

```
**What is the error and what is causing it in this program**
```

```
#### Step 2.

In this task you will be using American Fuzzy Lop (AFL), it is installed in the Kali Linux virtual machine. If you are using your own computer you can download it as follows:
```
~$ wget http://lcamtuf.coredump.cx/afl/releases/afl-latest.tgz
```
You can find the target program sourcecode following this link: [unrtf0.21.5.orig.tar.gz](http://http.debian.net/debian/pool/main/u/unrtf/unrtf_0.21.5.orig.tar.gz). This tool can be used to convert .rtf files into other, more readable formats (see README for more). Extract the package, **_configure_ it with appropriate AFL compiler flags and then _compile_**.

__Hint__: See AFL [quick start guide](http://lcamtuf.coredump.cx/afl/README.txt) for help

During this task, use the example .rtf file from AFL folder **.../afl-2.52b/testcases/others/rtf/small-document.rtf**. You can try that your unrtf is working properly using command line:
```
~$ /path/to/unrtf --html /path/to/testfile
```
Start fuzzing unrtf with AFL using the example .rtf file as input. See AFL [quick start guide](http://lcamtuf.coredump.cx/afl/README.txt) for instructions on how to start the fuzzer. Run the fuzzer, see what happens in the status window. Good description of the status window can be found [here](http://lcamtuf.coredump.cx/afl/status_screen.txt).

__Hint__: You are fuzzing a binary.

If you get an error regarding core dump notifications, try:
```
~$ sudo su
~$ echo core>/proc/sys/kernel/core_pattern
~$ exit
```
**Command line used to configure unrtf**
```

```
**Command line used to run AFL**
```

```
**Screenshot of the AFL status screen after stopping the fuzzer**
```

```
**What do you think are the most trivial pieces of information in the status screen?**
```

```
Did you find any crashes (you should)? Awesome! Next you need to reproduce one crash to see what went wrong. You can find the crashes where you specified the output folder when starting AFL fuzzer. Browse into the .../out/crashes folder, and take one .rtf file that caused crash under inspection. Runt unrtf with this file as you did with the example file earlier, but this time under Valgrind. Take a look at the Valgrind [documentation](http://valgrind.org/docs/manual/quick-start.html) for help.

**Take a screenshot of the Valgrind result after running a testcase succesfully**

![](img/Placeholder.jpg  "Add description here")

**What can you tell about the crash?**
```

```
## Task 3:

In this task you will write a small C program of your own and fuzztest it. In task 1 you created a .txt file containing "12 EF" and fuzzed samples of it, in this task we will use them. Your program must take a text file as an input and check the file for following requirements:
- First token is an **integer**
- Second token is a **string**
- Only two tokens are present
- If the content of the text file is as specified above, return code 0, otherwise 1

Compile and link your program with AddressSanitizer using appropriate flags.

Run your program with the previously generated 100 test cases. A simple shell script loop for example is an easy way to run the test cases.

**Provide the C-code of your program**
```c
paste here
```

**Take a screenshot of the AddressSanitizer results after running your program with the testcases. Show at least 3 ASan outputs.**

![](img/Placeholder.jpg  "Add description here")

## Task 4: WIP?
## Task 5: WIP?