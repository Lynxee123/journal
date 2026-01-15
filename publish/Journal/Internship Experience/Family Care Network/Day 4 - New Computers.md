---
tags:
  - internship
  - fcn
date: 1 / 13 / 26
hours: "4"
---
Fiber issues last night, but wasn't there for that. 

In with the new, out with the old! Today, we got some new Dell laptops to configure. 

### Windows Deployment via Intune

1. Insert USB with custom answerfile
	1. boot and open cmd to copy yaml file into auto
	2. shutdown /r /t 0
2. Once it finishes 

some things Ryan mentioned

running the answerfile once the laptop is connected to the Intune AD and in the event that someone steals it, it will always go back FCN sign in on the OOBE which basically makes it a brick if ever stolen.

the only way is if the device is intentionally retired and no longer in use. 

The computers always installed with these 3 things:
- intune
- tenable (nessus)
- Cisco Secure Client (does web filtering)
***rsm**, intune, tenable, cisco web filtering*
rsm is the third party provider for better security and any issues that need to 

after boot is complete, we run a powershell script that finds available computer names to rename the laptop. Desktops and Laptops have their own naming conventions > this is very important as it allows helpdesk when they need to remotely connect to a device

Then make 3 labels for the device of the device name: 
- top cover, middle of lower screen bezel, and charger

then we add teh new computer to the correct OU.

for example, one of the laptops was for a PAD manager. We look at a spreadsheet of the specific user and see if they already have a laptop.

we search that laptop up w/ NinjaOne and see what OU the user is already in and we can replicate those settings onto the new laptop.
	some familiar settings that basically all the laptops had:
	- 802.1x
	- bitlocker
	- imprivata
	- Specific department (e.g. PAD)

**After the OU group policy applied, run:**
```
gpupdate /force
```

### Update Kuiper

Gotta add the new workstation if not found
- move the device from POC to PRD

## Retired devices
Went through the process of retiring some laptops because it wasn't working anymore/there were issues. It was pretty simple- mostly documentation. 

Basically removing the device from AD, Kuiper, spreadsheet, etc. When that was done, I removed the SSD from the laptop

