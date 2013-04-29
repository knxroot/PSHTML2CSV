PSHTML2CSV
=======

You need convert html report from powershell to csv file?: This script is for you.

How you can use this?

1. First you need install Visual Studio >= 2010 and NodeJS, create "in" and "out" folders in the PSHTML2CSV folder.

2. Copy you html based report in "in" folder

3. Clone this repo in your computer and run "npm install & node c:\youfork\report2csv.js"

4. The CSV reports is now in "out" folder ;).

Example:


In Powershell
------
    Get-WmiObject Win32_PhysicalMemory -ComputerName $name  | select BankLabel,DeviceLocator,Capacity,Manufacturer,PartNumber,SerialNumber,Speed  | ConvertTo-html  -Body "<H2> Información de la memoria ram</H2>" >> "C:\PSHTML2CSV\in\mytest.html"
    Get-WmiObject Win32_Processor -ComputerName $name  | Select Name,Manufacturer,Caption,DeviceID,CurrentClockSpeed,CurrentVoltage,DataWidth,L2CacheSize,L3CacheSize,NumberOfCores,NumberOfLogicalProcessors,Status  | ConvertTo-html  -Body "<H2> Información de la CPU</H2>" >> "C:\PSHTML2CSV\in\mytest.html"
    cd C:\PSHTML2CSV\
    __npm install__
    __node report2csv.js__

