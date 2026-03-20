---
tags:
  - internship
  - fcn
date: 1 / 27 / 26
hours: "7"
---
Thirty-nine phones. One location. One very long Tuesday. The team headed out to Lynden Family Medicine for the big installation day!

The work itself started straightforward enough, pulling out the old phones and swapping in the new HP Poly Edge E350s. But it didn't take long before things got interesting. I went to connect one of the phones and it just wasn't getting power. I knew the Ethernet port had PoE capability, so something wasn't adding up. After some digging, the culprit turned out to be downstairs in the network rack. There were two FCN Cisco switches down there, but only one of them was PoE. The phone had been patched into the wrong one.

The fix was actually really satisfying to work through. We pulled up the Meraki web interface, found unused ports on the PoE switch that hadn't seen traffic in over a month, and moved the cables over. But that wasn't the end of it. Switching ports meant the configuration had to follow. Each port needed to be on the correct phone VLAN, and for any ports with passthrough to a computer or printer, we had to set the data VLAN correctly and reassign the VoIP VLAN separately. One of the printers also couldn't reach the phone for passthrough with its original cable, so I grabbed a 7-footer, made the connection, and cleaned everything up nicely. Then I tested it myself to confirm the printer was accessible. It was. There is truly no better feeling than troubleshooting something end to end and watching it work, especially when a teammate verifies your work and it checks out.

By 6:30 the whole team paused for a dinner break downtown, which was honestly a highlight. Good food, good company, and the important revelation that Ryan's favorite artist is Ed Sheeran.

The night wasn't quite done though. A cluster of phones in one area were refusing to contact the provisioning server, meaning they couldn't pull their extension numbers. After some investigation it turned out to be a two-for-one problem: a bad Ethernet cord AND some smaller switches tucked around the corners of the office that hadn't been configured to route the phone VLANs through their trunk ports. Once the VLAN settings were corrected and the ports cycled, the phones immediately reached the provisioning server and grabbed their extensions like nothing had ever been wrong.