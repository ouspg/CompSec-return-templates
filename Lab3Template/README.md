# Answer template for Lab 3: From innocent document file into part of botnet


Make a step-by-step report from what you did. (What, why and how?)
You can use screenshots, code snippets and anything, what Markdown enables you to use. Answer at least for the questions presented in each section.
They should be same than in actual instructions. 

You can add possible source files to [src](src) folder and screenshots to [img](img) folder.
You have to create these by yourself.

***You can remove questions and just leave task numbers/letters if you want.***

**Answer to this document, and push changes to Git!**

You can answer with more details than questions below are suggesting and describe anything what did you find and think that it is related to malware.


## Task 1: 

**A) Do we find some malicious files based on these? (ClamAV, VirusTotal) Even if there are malicious files, why might not they appear there? What is the bad thing on signature based identification? Include commands and steps how you did it.**


**B) What is the worst thing you can do with suspicious Microsoft Office document? (Disabled by default)**


**C) Malicious PDF files are also common. How they are usually infecting the machine of potential victim?**


**D) Which files are 'malicious' or doing something abnormal? What they attempt to do in general level? Are they executing some code? Include code. Include also the suspicious keywords of PDF. Include commands you used.**


## Task 2:

**A) What attachments email had? What was the content of message. Include possible commands and steps you did.**

**B) What document file is attempting to do general level? Could you figure out what macro is doing?**

**C) Document is actually containing binary. How it is stored inside document, and how it was used? Include step(s) you did to acquire the binary.**

**D) Let's take a look for this binary. *Make a brief explanation of the functionality*. How it attempts to persist in the system and evade detection? It downloads also some file, but no need to analyse that  yet, that will be handled in the next task.**

## Task 3:

* Make general level analysis of the file. As a tip, it attempts to make user part of botnet
* This file contains actually two additional binaries. What are their names? How did you got them?
* **Find a way** to reverse these files as well, and include the general purposes of these files as well to your report. Additionally:
  * How bots were controlled? There were at least two ways, describe at least the automatic approach.
  * Some source code or ideas of some common DDoS tools have been used in this malware. Describe three of them. It's enough to identify tools, you can look information about them elsewhere.
  * Malware actually contains hidden GUI for DDoS tools it is using. Can you find and use it? Describe how you did it.



## Task 4:

**Make step-by-step report (what, why and how) for what you did. Include possible source and configuration files as well.**