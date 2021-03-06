# Preformance testing:

## Customer profiling 
![image](https://serendipity2.com/s2web/wp-content/uploads/2017/04/Customer-Profiling.jpg)
Consumer profiling (also referred to as "customer profiling") is the only way to gather the insights needed to identify, segment and define your target audience.

 - Set the bussiness expectations of the product 
 - align the customers expectations with the product \


# Tests theory
 - Tests are conducted in order to make sure that the site is allways available.  
 - it takes 6-12 weeks to do a test depeing on the level of the system that need to be tested
## Tools for Tests: 
- Gattling - open source testing software 
## Types of Tests: 
 - *load Test* - tests help you understand how a system behaves under an expected load
 - *spike Test* - application receives a sudden and extreme increase in requests
 - *stress Test* -tests help you understand the upper limits of a system's capacity using a load beyond the expected maximum
 - *soak Test* - Testing a system with a typical production load, over a continuous availability period, to validate system behavior under production use.

## Itterative approach 
### Preformance tesing in 3 steps:
    - identify cases
    - align test cases with functinality 
![image](https://www.smartsheet.com/sites/default/files/IC-Iterative-Process.jpg)

### To do:
    - install java
    - install scala plug in 
    - install intellij
    - install gattling

## installations and configure:
## Part 1:
To do:
install Java version 8 and up.
this can be checked using the `java -version` command in java:
```
java version "1.8.0_201"
Java(TM) SE Runtime Environment (build 1.8.0_201-b09)
```
if this doesnt work, you will need to install Java and configure the path file. you can do this by following this link. 
___

[install-java-windows link](https://devwithus.com/install-java-windows-10/)

## Install The lastes version of intellij:

[intellij download link](https://www.jetbrains.com/idea/download/#section=windows)


## install `scala` as a plugin in intellij
![image](https://devskiller.com/wp-content/uploads/2018/05/Scala-Blog-post.png)

## Download Gattling:
use this link and place it somewere you can access it

[Downaload the document](https://gatling.io/docs/gatling/tutorials/installation/)

___
# Test section
This section will cover how tests are conducted:
- recording the website tasks that you want to test 
- 


This is a stress test meaning that the website will have lots of requests sent to the website. This is a DDOs attack, so you ` MUST OWN THE WEBSITE YOU ARE TESTING `


Go to the website that you want to test e.g.: 

![images](https://github.com/ViMitre/sre_gatling/raw/main/img/1.png)



1. left click on the webiste and select insect. 

2. click on the network tab

![image](https://docs.appdynamics.com/download/attachments/31820071/HARone.png?version=1&modificationDate=1418933961000&api=v2)

3. press the record (red) button then run thought the site doing the activites. 

4. After you are done, stop the recoding and download the HAR file, by pressing the download button and save in your local space. 

## Intelij scala test

open a terminal and change dictinary into the gattling *bin* file then type:

` ./recorder.bat`

then you should see :
```
GATLING_HOME is set to "C:\Users\pauli\Desktop\gatling"
JAVA = ""C:\Program Files\Java\jdk1.8.0_201\bin\java.exe""
```
then this page will pop up:

![image](https://gatling.io/docs/gatling/reference/current/http/recorder/images/recorder.png)

- In the top right "Recorder mode" change the `HTTP proxy` to `HAR convertor ` then the gattling software will chnage to this:


![image](https://automationrhapsody.com/wp-content/uploads/2015/09/Gatling-recorder-HAR.png)

- Click brows and enter the place the HAR file that you downloaded. 

- Once the file has been incerted press `start` at the bottom right.

once it has fininshed go back to intelij

## Running the test

once in intelij 

In the same location that you ran  `./recorder.bat`
there should be a file called `./gattling.bat`
run that command. once the command has been run, then you should see a list of recodings like this:
```
$ ./gatling.bat
GATLING_HOME is set to "C:\Users\pauli\Desktop\gatling"
JAVA = "java"
Choose a simulation number:
     [0] AwsSpartaInstance 
     [1] RecordedSimulation
     [2] Testnewhar
     [3] computerdatabase.BasicSimulation
     [4] computerdatabase.advanced.AdvancedSimulationStep01     
     [5] computerdatabase.advanced.AdvancedSimulationStep02     
     [6] computerdatabase.advanced.AdvancedSimulationStep03     
     [7] computerdatabase.advanced.AdvancedSimulationStep04     
     [8] computerdatabase.advanced.AdvancedSimulationStep05     
     [9] proxyTest


```
Select your recoding and wait for the tests to be completed.

Once the tests are completed. Navigate to the gatling `user-files\simulations` and click on the newly created file. 
click on the `index.html` file



![image](https://cdn2.hubspot.net/hubfs/208250/Blog_Images/gatlingapi2.png)

## AWS cloud watch

![image](http://cdn2.hubspot.net/hub/208250/file-2237421292-png/Blog_Images/AWSblog1.png?t=1418810526863)

## What gets monitored 
### Monitoring

Adding more hardware to a server to make it bigger in order to increase its load will need to be monitored in ordered to make sure it works.
- Things that need to be monitored:
    - Computer Resource: \
    RAM usage, CPU load, and remaining disk space.
    - Network :\
     firewalls, servers and switches 

## GOAL --> To achieve Highly Availability and Scalability

