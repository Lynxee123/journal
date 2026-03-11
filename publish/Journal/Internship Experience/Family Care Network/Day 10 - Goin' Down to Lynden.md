---
tags:
  - internship
  - fcn
date: 1 / 27 / 26
hours: "7"
---
- Set up 39 new phones at the LFM
- Learned about how the Ethernet ports in the office lead down to the network rack into a patch panel and that into the switch.
- I did one of the phones but the Ethernet port was not giving PoE even though I knew it existed. I then figured out that it was because the switch that it was connected to downstairs in the network rack was not PoE- see, the network rack had two FCN switches; however, only one was PoE:
	- wanted to make sure that the phones were utilizing PoE when possible, but while FCN had two cisco switches in the rack, only one was PoE. So we went into the meraki web interface and found any unused ports on the PoE switch within the past month and moved the cables there. 
	- For the phones that fed into the Ethernet port that had the switch ports changed, the configuration also had to be changed
		- Made sure the port was on the correct phone VLAN
		- If there was any passthrough from the phone, then the port had to be on the VLAN the computer or printer required and changed the VoIP VLAN instead as well
	- After that was done, I also had to get a new Ethernet cable because the printer in the room couldn't reach the phone for passthrough with its original cable - got a 7ft and got it nice and cleaned up! It was really satisfying that I understood how it worked and did it by myself (but with verification from another team member).
	- Tested to make sure the printer was accessible and it was - yay!
- Once it hit 6:30 PM, the whole team took a break to get dinner. It was really nice down town to interact with everyone. Like Ryan's fav artist is Ed Sheeran lolz.
- There was a certain area where the phones weren't able to contact the provisioning server to get the correct extension numbers. After investigation, we found that there were multiple issues:
	- Bad Ethernet coord
	- Trunk port of the switches (not the same ones as the network rack ones, they were smaller and hidden around the corners) was not configured to route the phone VLANs. So once that was changed correct and the port cycled, then the phones were instantly able to contact the provisioning server and get the correct extension number. 