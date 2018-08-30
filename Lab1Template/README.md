# **Answer template for Computer security lab 1: Fuzzing**

Fill in your answers to this template, answer every question. If screenshots are required, add them to "img" folder. Example of how to add images can be seen at the end of task 2.

If your own code is required, you can paste it to this document or create a "src" folder and add your code there.
## **Task 1**: Mutated test case generation with Radamsa

**A)** 

**Provide the command line you used to do this.**
```
```

 **B)** 


**Provide the content of 2 different samples that radamsa created**
```
```

**Command line used to create the samples**
```
```
---
## **Task 2**: Analyzing a C-program with AddressSanitizer, fuzztesting with AFL
**A)** 

**Command line used to compile the program**
```
```
**Screenshot of the result after running the program**

![](img/Placeholder.jpg  "Add description here")


**What is the error and what is causing it in this program**
```
```
---

**B)**

**Command line used to configure unrtf**
```
```
**Command line used to run AFL**
```
```
**Screenshot of the AFL status screen after stopping the fuzzer**

![](img/Placeholder.jpg  "Add description here")

**What do you think are the most trivial pieces of information in the status screen?**
```
```
---
## Reproducing a crash:

**Take a screenshot of the Valgrind result after running a testcase succesfully**

![](img/Placeholder.jpg  "Add description here")

**What can you tell about the crash?**
```
```
---
## **Task 3**: Creating your own small C-program and fuzztesting it



**Provide the C-code of your program**
```C

```
**Take a screenshot of the AddressSanitizer results after running your program with the testcases. Show at least 3 ASan outputs.**

![](img/Placeholder.jpg  "Add description here")

---
## **Task 4**: Contribute to a existing open-source project. Set up a fuzzer and report findings.

Contribute to an existing open-source software (OSS) project by setting up a fuzzing environment and documenting the process and results. You can choose the target software by yourself and use one of the 2 fuzzers introduced during the lab exercise, or pick some other that you think serves the purpose better. 

You should read for example [this guide](https://github.com/ouspg/fuzz-testing-beginners-guide) to get started. Please note that in case a real bug is found in the software, it is very important to document the results in a way that the issue can be easily reproduced. The guide has some good pointes of what information you should provide.

To be continued.. Work in progress.
