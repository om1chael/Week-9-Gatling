# Preformance testing:
## Customer profiling 
![image](https://serendipity2.com/s2web/wp-content/uploads/2017/04/Customer-Profiling.jpg)
 - Set the bussiness expectations of the product 
 - align the customers expectations with the 


### 6-12 weeks to do a test depeing on the level of teh system that need to be tested

## Tools: 
Gattling (open source load testing software) 
## Types of tests: 
load, spike , stress  and soak

## Itterative approach 
### Preformance tesing in 3 steps:
    - identify cases
    - alighn test cases with functinality 

![image](https://www.webairy.com/wp-content/uploads/2019/07/hvsv.jpg)

## Local Configure:
To do:
install Java version 8 and up.
this can be checked using the `java -version` command in java:
```
java version "1.8.0_201"
Java(TM) SE Runtime Environment (build 1.8.0_201-b09)
```
if this doesnt work, you will need to install Java and configure the path file. you can do this by following this link. 

[install-java-windows link](https://devwithus.com/install-java-windows-10/)

Install The lastes version of intellij:

[intellij download link](https://www.jetbrains.com/idea/download/#section=windows)

 install `scala` as a plugin in intellij

download Gattling:
use this link and place it somewere you can access it

[Downaload the document](https://gatling.io/docs/gatling/tutorials/installation/)


## Test section
This section will cover how tests are conducted:
- record the website tasks that you want to test 
- increase the user  


This is a stress test meaning that the website will have lots of requests sent to the website. This is a DDOs attack, so you ` MUST OWN THE WEBSITE YOU ARE TESTING `


Go to the website that you want to test e.g.: 

########## \
ADD SPARTA IMAGE\
##########



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

- once the file has been incerted press `start` at the bottom right.


## Testing the 