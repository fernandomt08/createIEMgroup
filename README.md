# createIEMgroup
An example I developed for a particular Airline, using either python or powershell to create groups in BF from names in a text file

An example of how it is used (see docs subdirectory for .gif of resulting console <note that it shows a different
number of member computers, b/c it was taken before member computers 'reported back in'; also, sorry for the
misspelling of the group name>):

$ createIEMcomputerGroup.py MyBlahGrojp computer_group_members.txt -u adminMO -p adminmo

Heres the response XML about the action that I invoked:
<?xml version="1.0" encoding="UTF-8"?>
<BESAPI xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="BESAPI.xsd">
        <ComputerGroup Resource="https://grasskeet:52311/api/computergroup/master/5965" LastModified="Wed, 16 Sep 2015 15:47:23 +0000">
                <Name>MyBlahGrojp</Name>
                <ID>5965</ID>
        </ComputerGroup>
</BESAPI>

The python version uses the excellent requests library (note that as of this date, running the script will 'complain' 
that 'an unverified HTTP request is being made'.  This can be quiesced by modifying the code, but it's better if you
change the code to use an actual SSL token if you do something like this in a production environment).

Note that there are two versions, here, one in python (in which I originally developed, to 'prove the concept', and
powershell, which is what the customer asked for).

[I describe my thought-process on how I created this on my blog (called 'Lesson 5') at: https://www.ibm.com/developerworks/community/blogs/edgeCity/?lang=en]

-jps
