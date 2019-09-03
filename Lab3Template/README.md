# Answer template for Lab 3: Botnes and malwares


Make a step-by-step report from what you did. (What, why and how?)
You can use screenshots, code snippets and anything, what Markdown enables you to use. Answer at least for the questions presented in each section.
They should be same than in actual instructions. 

You can add possible source files to [src](src) folder and screenshots to [img](img) folder.
You have to create these by yourself.

***You can remove questions and just leave task numbers/letters if you want.***

**Answer to this document, and push changes to Git!**

You can answer with more details than questions below are suggesting and describe anything what did you find and think that it is related to malware.


## Task 1: Malware - dynamic analysis

NOTE: No need to answer  anything for A section. I was just a little tutorial for sandbox environment.

### B) Dynamic analysis

* Based on analysing network traffic and connections - shortly describe what malware is doing
  * Malware is connecting to some domain, which one?
  * What it did at first with domain?
  * After that, some kind of harmful cycle started. Can you describe it?
  * Describe which details in result files gave required information

```
You can insert text in here.
```

* Compare start and end logs in memlogs folder

  * What are mutexes in programs, and why are we analysing them?
  * Which new processes were spawned?
  * If you compare mutexes, what are they telling about the program we launched? 
  * What are differences in netscans telling?
   * If you used any volatility plugins manually, did you find something else interesting?

```
You can insert text in here.
```


* Based on disk analysis, can you guess what files malware created? What entries in registry it edited? Why it was useful for malware to edit these entries?

```
You can insert text in here.
```

### C) Inspecting the server (Command & Control center)

* What exact information bot got from the server?

```
You can insert text in here.
```

* You can give code/commands here for receifing traffic or additionally put it into *src* folder.
```python
You can insert your code here
```
* Provide screenshot, when it is receiving data. You can put it in *img* folder and reference here.

## Task 3: Malware - static analysis

### A) What's the role of SteamCodeGenerator.exe, keycrack.exe and steam-dll-pro.exe?

### B) How are they trying to hide their current/upcoming activites?

* For example, did they edit some settings in the operating system?

### C) What's the role of anti-cheat-bypass-tool.exe in Data folder?

* We are particularly interested about this file.
* This file contains actually two additional binaries. What are their names?
* **Find a way** to reverse these files as well, and include the general purposes of these files as well to your report. Additionally:
  * How bots were controlled? There were at least two ways, describe at least the automatic approach.
  * Some source code or ideas of some common DDoS tools have been used in this malware. Describe three of them. It's enough to identify tools, you can look information about them elsewhere.
  * Malware actually contains hidden GUI for DDoS tools it is using. Can you find and use it? Describe how you did it.

### D) How well you were able to gather information from malware with dynamic analysis when compared to full reveal from source code? (optional question, does not affect grade)


## Task 4:

**Implement **one** of the described tasks, and make step-by-step report (what, why and how) for what you did. Include possible source files to *src* folder.**