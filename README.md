# Lenovo-BIOS-Settings
Disclaimer: You will still have to set the BIOS Supervisor Password manually if there is not one already on the device.

The BIOS Password changing script will input the current BIOS Supervisor Password and change it to the value stored in $newpassword. It will then provide feedback to the user on what happened. The changes will be saved but will not take place until you reboot your device. 

The detection and remediation scripts will let you manage BIOS settings for your Lenovo device using PowerShell. They will detect your current settings and compare them to the "Good" values listed in the variable $CSV_wordbank. Essentially it creates two temporary csv files and compares them side by side. Those not in line with the "Good" values listed in the CSV_wordbank will be displayed to the host or changed depending on if you used the detection or remediation script. If the setting does not exist it will return "Failed to change (insert seting Name,Value)" then it will move to the next value. There is a spot for the BIOS password if you configured a Supervisor Password for your device. I left mine as "Supervisor" under the $BIOSPassword variable to make the location easier to find in the script. At the end of the script it deletes the temporary files that it created. 

These scripts work well with Proactive remediations in Microsoft Intune/Endpoint if you are a system administrator. 
