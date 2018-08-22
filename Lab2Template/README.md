# Network lab return

**Name:** ```Fill here ```

**Student number** ```Fill Here ```

## Instructions

Below is a copy of the questions found in the Network lab folder. Answer the questions here. In task 4 put the server code and the XSS-script to a different file. Also the picture and the report in task 5 can be returned as a separe files. 


### A) Basic SQL Injections

**Noticing errors**


What command(s) did you use?
``` sql

```
Explain each command/symbol you used.  Why do they cause an error?
```sql

```
 
Paste here the command that the SQL server attempts to execute and replace the part(s) taken from the searchfield with the text "SEARCHRESULT". 
``` sql

```
---
**A bit more concrete error**


What command(s) did you use?
```sql

```
Why it is working/what is happening?
```text

```

---


What SQL command did you use?
 ``` sql

```
How are the items "deleted"?
```
```


Explain shortly the logic behind your attack. Why does it work?
```

```


### B) Modification of client-side code

**Admin section**


What is the url to access administration panel? You can find page even, when you are not logged in, but information is not showed. Why this still could be considered as risk?
```
```

---


How did you do it? Why you were able to?
```
```
---
**Scoreboard**

How did you make it visible?
```
```




## Task 2 


What SQL command did you use?
 ``` sql

```

Explain shortly the logic behind your attack. Why and how does it work?

```

```

Put an item to your basket and checkout. Monitor the traffic using your browsers devtools. By modifying the requests it is possible to checkout with negative amount of items. Proceed to do so.

How did you do it?
```
```


What is the difference between these two types of attacks? How can you protect your applications against both types of attacks?
```
```

*short explanation on how you did it*  
```

```

### Brute forcing

Next we do some basic brute forcing.Do the following:
* Start muumitalo.  ```git clone https://github.com/VilleKemp/Muumitalo``` follow the instruction on the git page on how to start it. You will be bruteforcing this server
* Create a wordlist containing mutations of the word "vaapukkamehu". Create mutations where individual letters case changes between upper and lower case. Also make mutations where letter 'a' can be number '4' and letter 'e' can be number '3'. 
* Brute force the right answer to the question posed by the server using above mentioned wordlist
You can use any tools you find online. If you want to, you can code your own mutator. Alternatively you can search online for a existing mutator/mutators and use them to create the wordlist. Same thing with the actual attack. You can use programs like [OWASP ZAP](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project) to do the actual attack after you have created the wordlist.
#### Returns
* Wordlist
* Any code you created.
* Detailed description on how you created the wordlist and how you did the brute force attack.

__Hint__ Internet is full of tools to create wordlists. It is potentially easier to combine multiple tools to create the wordlist. You can use existing tools to do the attack if you don't feel like creating your own script. [OWASP ZAP](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project) for example can do the attack easily if you have a list containing all the mutations. Don't try to do the attack using burp community edition. It does not allow you to use files as payloads.

## Task 3

The XSS attack you did in the previous task was mostly just annoying. It could however have been way more malicious. Next we are going to do just that and modify it to be way more dangerous. Your task is the following:

* **Setup a server.** No need to do anything fancy. Basic python flask/http server that can receive post requests is fine. Server can print or save the information to a file. Anything goes as long as it shows that the data entered the server.  
* **When the user accesses the administration panel the page will look like the login page.** Page should be as similiar as possbile but small differences are fine. For example slightly different size login fields, email field not checking for @ sign etc.
* **When the user inputs anything to the email and password fields and presses the *Login*-button all the information in the email and password fields are sent to your server.** The way you send/show the information is up to you. You just have to demostrate in the server side that the data has entered and that it is the same as inputted to the email and password fields.

### Returns

* Server code
* Request you send to the server in a separate file
* **Clear** instructions on how to start the server, send the Cross-Site script attack and how to verify that the information was sent to the server. 


__Tips__  
Refresh your mind how javascript can modify html elements.

It is also handy to use programs like [curl](https://curl.haxx.se/) to send your XSS-scripts.

Keep in mind that the user database is purged each time you restart the Juice Shop. If you break the system just reboot the docker container.

You will likely need to format your request so that the servers JSON parser will accept it. Feel free to use tools like https://www.freeformatter.com/json-escape.html


## Task 4

You can complete this task in two ways. You can do the predefined task explained below or you can suggest a task that interests you and do that. __Contact the course assistants__ and describe them what you are interested on doing/trying to do. If they say it is good you can do that as your task 4.

## Predefined task

### Setup

Start the example-voting-app
```
cd example-voting-app
docker-compose up
```
### Task
In this task you are expected to learn to capture traffic using WireShark and to do very basic network analysis. With the knowledge you gain you are then expected to draw a data flow diagram on how the system behaves when you cast a vote or check the results. After this you try some form of a security experiment(for example modify traffic using burp). Report your result even if you are unsuccesful. 


__Hint__
 You can draw the diagram by hand and take a picture (asuming that the picture is clear enough) or use any tool you like to draw it. 
Scan networks (docker network ls, docker network inspect examplevotingapp_*, nmap 172.xx.0.0/24)
Look at  https://github.com/dockersamples/example-voting-app for architecture diagram (good basis for DFD)
Use wireshark on the two docker networks to see what happens when a vote is attempted
 

 
To run Wireshark correctly without using straight root priviledges, we should add current user to group *wireshark* with following command:
```shell
sudo usermod -a -G wireshark compsec
```
Log out and log in, wireshark should show now all interfaces.


 ### How to complete this task

Return the following:

* Data flow diagram or some other type of picture/written document that explains the dataflow in the situation where you cast a vote and when you check the results

* Short explanation on the steps you took to analyze the network and create the diagram

* Short explanation on what kind of security experiment you tried, how you did it and what was the result





























