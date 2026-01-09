---
tags:
  - internship
date: 1 / 9 / 26
---
Finished up on some new hire on-boarding this morning. 

Went to the Family Health Association (FHA) building and helped move some computer set ups to a different room. Just plugging in monitors, keyboards, mice, etc.

Shadowed the system admin (Ryan) and introduced the Microsoft admin center: Entra, Intune, Purview, etc. A process he was showing was when someone gets a spam email.

Goal: Delete the email remotely - Derrick could most definitely delete the email himself, but if the email was sent to multiple people, we want to verify this and ensure that the email is deleted from every user who received it. TL;DR we can't trust that everyone would actually remove so we must do it ourselves. 

It was interesting to see the step by step process of this. Using Microsoft Admin Center:
1. Filtered for all emails that went to Derrick around the time frame the email was sent
2. Found the specific spam email that was sent to Derrick
3. Filtered to find if the email was sent to any other users (in this case, it was only to Derrick)
When Ryan attempted to delete the email, however, it became tricky- not due to Ryan, but because Microsoft just loves renaming and moving things around so that by the time you know where something is.... well, not anymore :P

Solution? GTS! In the end, it was looking at good ol' Microsoft documentation and putting in some commands in Powershell. 