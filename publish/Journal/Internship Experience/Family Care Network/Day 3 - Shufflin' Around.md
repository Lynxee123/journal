---
tags:
  - internship
  - fcn
date: 1 / 9 / 26
hours: "8"
---
I finished the last of my new-hire onboarding this morning and then headed over to the Family Health Association (FHA) building. I helped move some computer setups to a different room. It was standard IT work involving a lot of plugging in monitors, keyboards, and mice.

Later, I shadowed the System Admin, Ryan. He introduced me to the Microsoft Admin Center, specifically Entra, Intune, and Purview. He showed me the protocol for when a spam email hits the network. The goal is to delete the email remotely. Even if a user says they deleted it, we have to verify if it was sent to anyone else to ensure it’s wiped from every inbox. We don’t leave security to chance.

**The process was interesting to watch:**
1. Filter for all emails sent to the user during that specific timeframe.
2. Identify the exact spam message.
3. Run a wider search to see if any other users received it.

When Ryan tried to execute the delete, things got a bit tricky. Microsoft loves to rename and move menus around frequently. By the time you memorize where a tool is, they have often moved it. 

The solution? GTS! We pulled up the latest documentation and used PowerShell to finish the job via the command line.

We wrapped up the week with a team meeting. Some notes:
- We are installing about 30 phones at Squalicum Family Medicine
- Got asked some fun initiation questions:
	- Dog or Cat? Apple or Android? Burger or Pizza? I'm pretty sure I passed that with flying colors :)

