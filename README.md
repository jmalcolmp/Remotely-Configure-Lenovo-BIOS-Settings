# Lenovo-BIOS-Settings-Detection
This script will let you manage BIOS settings for your Lenovo device using PowerShell. Included in the Repository is a script for detecting your current settings and comparing them to the "Good" values listed in the variable $CSV_wordbank. Essentially it creates two temporary csv files and compares them side by side. Those not in line with the "Good" values listed in the CSV_wordbank will be displayed to the host or changed depending on if you use the detection or remediation script. 

There is a spot for the BIOS password if you configured a Supervisor Password for your device. I left mine as "Supervisor" to make the variable that inputs the current supervisor password more obvious. In regards specifically for the remediation and detection script, at the end of the script it deletes the temporary files that it created. 

These scripts work well with Proactive remediations in Microsoft Intune if you are a system administrator. 
