---
tags:
  - internship
  - fcn
date: 1 / 29 / 26
hours: "4.5"
---
Fresh off the Lynden installation high, Thursday brought a new problem to solve. Reports were coming in from SFM and IFP about phone calls dropping and phones going offline. 

We pulled up the phones and started watching the QoS metrics, and a pattern emerged pretty quickly. The phones connected over WiFi were the ones struggling to hold a stable connection. Wired phones? Fine. Wireless ones? Not so much. It's one of those situations where the root cause makes total sense in hindsight. WiFi and VoIP are not exactly best friends, and in a busy clinic environment with a lot of competing traffic, the cracks start to show fast.

Derrick jumped in with a plan. To get a clearer picture of what's going on and where, he asked us to put together a shared Excel document with four sheets: two clinics, two sets of the same information. Each sheet tracks every extension and how it's connected, whether that's wired Ethernet, Streamline, or wireless. The second sheet for each clinic is a running log of reported call issues, capturing the extension, the time, and what actually happened. It's a simple but smart way to start mapping the problem before trying to fix it.

The honest hindsight here is that ideally all the phones would have been wired in from the start. A dedicated Ethernet connection per phone would have avoided all of this. But running that much cable has a real cost attached to it, and sometimes budget realities shape technical decisions whether you like it or not. For now, the spreadsheet will have to do. 