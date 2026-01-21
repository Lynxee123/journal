---
tags:
  - internship
  - fcn
date: 1 / 13 / 26
hours: "4"
---
I missed out on some fiber cable drama last night, though it sounds like there wasn't much the internal team could do about it anyway. Instead, I spent the day getting on with the new and out with the old. We had a batch of new Dell laptops to configure using Windows Deployment via Intune.

The process is pretty slick. We use a USB with a custom answerfile that automates the setup. Once the laptop connects to Intune, it’s basically tied to Family Care Network forever. Ryan explained that even if the device were stolen and wiped, it would still default back to the FCN sign-in screen at boot. It essentially becomes a brick unless we intentionally retire it from our system.

**Every machine gets the "Big Three" installed automatically:**
- **Intune** for management
- **Tenable (Nessus)** for security scanning
- **Cisco Secure Client** for web filtering

After the install, we run a PowerShell script to find an available name based on our naming conventions. This is huge for help desk so they can actually find the device later to remote in. Then comes the labeling (cover, bezel, and charger) and adding it to the correct OU (Organizational Unit). We use NinjaOne to see what groups the user is already in and replicate those settings. A quick `gpupdate /force` later, and the new laptop is ready for the field.

I also helped retire some old devices. It’s mostly documentation—removing them from AD and our spreadsheets—but the "physical" part is the best. I got to pull the SSDs out of the laptops and toss them in the E-waste drawer.