---
tags:
  - internship
  - fcn
date: 1 / 23 / 26
hours: "8"
---
Friday meant help desk duty, which meant finally getting some real hands-on time with NinjaOne and the ticketing system. The call that came in was about a contact in Outlook that kept reappearing after being deleted. After doing some googling, the fix was to delete it through Outlook Web instead of the desktop app, which then overrides the local version and actually makes it stick. Problem solved!

The meatier part of the day came when Ryan pulled us back into switch configuration territory. Today's topic was 802.1x, which is port-based network access control, basically the bouncer at the door that decides which devices get onto the network. He walked us through how it connects with their RADIUS server, and the concept of a "shared secret" came up as a big piece of that puzzle. It's the key that lets the switch and the RADIUS server trust each other. The whole setup is designed to make sure only FCN devices can join the FCNnet WiFi, which makes a lot of sense in a healthcare environment where you really, really don't want random devices poking around.

Of course, nothing goes perfectly on the first try. When adding the new switch to the RADIUS server, it turned out there was no DNS record for it yet. A classic "how is it not finding it" moment that had a very simple answer once you knew where to look. And as the old adage goes:

![[Pasted image 20260123150026.png]]