---
tags:
  - internship
  - fcn
date: 1 / 9 / 26
hours: "8"
---
I wrapped up the last of my new-hire onboarding this morning, which meant it was finally time to get out of the building and do something. First stop: the Family Health Association. The mission? Moving computer setups to a different room. Not exactly the most glamorous work, but there is something weirdly satisfying about getting a whole workstation untangled, relocated, and plugged back in perfectly. Monitors, keyboards, mice, the works. Humble work, but it counts.

The real highlight of the day came when I got to shadow Ryan, the System Admin. He pulled back the curtain on the Microsoft Admin Center, specifically Entra, Intune, and Purview, and walked me through what happens when a spam email lands in someone's inbox. In this case, the lucky recipient was Derrick, the IT Manager himself. The goal is simple in theory: delete it remotely. But the catch is you can't just take the user's word that they deleted it. You have to verify whether it was sent to anyone else and make sure it's wiped from every inbox. We don't leave security to chance.

The process was actually really interesting to watch. You filter for all emails sent to the user in that specific time window, identify the exact message, then run a broader search to see if anyone else got it too. Clean and methodical. Except then the unexpected happens: Microsoft decides to change their UI again! Truly every tech's nightmare. 

Ryan went to execute the delete and the menu had moved. Again. Apparently this is just a regular occurrence because by the time you memorize where a tool lives, it's already packed up and relocated. The solution was to pull up the latest documentation and finish the job through PowerShell instead. Yippee for adaptability!

We closed out the week with a team meeting. Big news: we're installing about 30 phones at Squalicum Family Medicine, so that provisioning work from Thursday is about to pay off. I also got hit with the real initiation questions: Dog or cat? Apple or Android? Burger or pizza? I wasn't quite familiar with that type of interview style, but it's safe to say I passed with flying colors. 

