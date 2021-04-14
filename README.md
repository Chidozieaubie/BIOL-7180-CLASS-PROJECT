# BIOL-7180-CLASS-PROJECT
## About this Project:
This is a class project for BIOL7830-a graduate-level course designed to help biologists and other life-scientists get comfortable at coding.

## Function
This repo contains a python script that enables one to search a select  online stores for the Sony PS5, the latest console in the Playstation series.
The script is dynamically built to allow users _scalp_ select stores -Best Buy, Sony Direct and Target for the PS5 console. The script allows users to receive email prompt as well as SMS alerts when games are available from the stores. 

## Required Software and Variables

* Smtplib
*	SSL
*	Selenium
*	BS4

You can do:  pip install -r requirements.txt if you want to install everything needed

To get notifications, you will need to have two emails; sender and receiver addresses. I have set this script to use the google SMTP-SSL protocol, so you must use a gmail address as a sending address. Your email’s password can be hardcoded into the script or typed in from the command line. I commented on both options in the script. The former option allows you to have a Task Scheduler run the script at user-set intervals without the inconvenience of having to type in password all the time. 
Secondly, you will need to input a phone number that you wish to get sms alerts from, as well as their corresponding carrier.   In the script, I provided a reference to some of the major mobile carriers and their domain names to help you.
Lastly, this script uses Selenium (for browser automation), hence you will also need to have isntalled google Chrome (or the lite version-Chromium) and Chromedriver. input the chromedriver path on your computer to the script before you run it. Here is a [link](https://chromedriver.chromium.org/downloads) to the chromedrivers. Download the one relevant to your chrome browsers version, and use the path for the script. I also found [this website](https://tecadmin.net/setup-selenium-chromedriver-on-ubuntu/) useful for installing the dependencies on Ubuntu. 
## Task Scheduling
To have the script to continue to run in the background, you can use the nohup command:
for Linux the command nohup python `nohup /path/to/test.py &` is used, while for Windows `pythonw.exe test.py`. You can kill the process with `kill PID` or `pkill -f test.py`
Alternatively, you can use the Windows Task Scheduler if you are using a Windows to run the script at user defined intervals. 
