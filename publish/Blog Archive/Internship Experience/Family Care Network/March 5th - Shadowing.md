---
tags:
  - internship
  - fcn
date: 3 / 5 / 26
hours: "4.5"
---
If Tuesday was seventy-eight phones, Thursday was a full on deep dive into what Vir, FCN's web admin, does day to day!

The center of it all is EPIC, the electronic health record system that basically everything else orbits around. But what I didn't fully appreciate before today is just how much infrastructure it takes to keep EPIC running smoothly. There are fifteen different EPIC environments alone, including training, production, disaster recovery, and reporting. The reporting environment is its own thing because EPIC doesn't run on a traditional relational database, so Jeff (another EPIC administrator) manages a whole separate SQL setup just to format the data into usable reports. And because medical data is constantly changing, things like prescription records are ephemeral by design, getting wiped from reports every two to three days.

Then there's the question of what happens when production goes down. FCN has that covered too. If prod is down but the network is up, clients can connect to a read-only version of Hyperspace through the reporting environment. If the internet itself is up but prod is down, there's BCA web as a fallback. Redundancy on top of redundancy, which makes a lot of sense when the alternative is a clinic that can't access patient records.

Hyperspace and Hyperdrive sound like they should be the same thing but they're actually solving different problems. Hyperspace opens a session on George's (another EPIC admin) servers and spins up a Citrix container with peripheral passthrough, great for most users. Hyperdrive is a local installation designed specifically for exam rooms where multiple providers share the same computer. Instead of constantly switching profiles through a session, everyone just uses local profiles. Clean solution for a very specific workflow.

Citrix is the glue holding a lot of this together, providing a centralized place to manage and update everything, with a Netscaler ADC handling load balancing. Vir is currently working on implementing rate limiting and building out DoS attack protection for the Netscaler, which is running in a high availability pair. Vir's day to day is a mix of Tenable Nessus for endpoint management, support logs, checklists, and a couple of active projects including web BLOB storage migration.

New EPIC versions come with NOVA notes, and before anything gets pushed to production there's a whole meeting with representatives from different departments to decide what's critical, what's wanted, and what can wait. 

Epic Print Service routes all printing through a central service that Vir can search and audit, which is a surprisingly powerful troubleshooting tool. Everything runs on VMware as the hypervisor underneath it all, with System Pulse keeping an eye on the health of the servers. And for security, FCN brings in a third party for penetration testing and audit reports through RSM.

All in all- out of everything that was mentioned, Vir made sure we understood: As IT professionals, having a separate ech support is the best.