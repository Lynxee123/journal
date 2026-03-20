---
tags:
  - internship
  - fcn
date: 3 / 5 / 26
hours: "4.5"
---
shadowing VIr

Components:
- Kuiper
	- doesn't see anything that isn't EPIC
- Citrix
- VSphere
- SystemPulse
- Hyperspace
- Hyperdrive


- Kuiper > management
	- different servders
	- Jeff has a bunch of analytics
	- EPIC Environments (15)
		- training
		- prod 
			- DR
			- Reporting (Jeff) > he manages SQL database for any kind of reporting
			- basically epic doesn't run on a relational DB so you need to format it to make reports
			- Data is very ephemeral > reports are deleted 2-3 days (e.g. a prescription could be changed)
	- when prod env is down, cleints can use read only hyperspace > connect to RPT
	- if prod down but internet up > can use BCA web
	- Citrix > docker containers > when Hyperspace is open spins up container
		- George manages Citrix and Hyperdrive
- Hyper drive vs Hypersapce
	- Hyperspace: opens a session, spins up container > passthrough of peripherals on the session
	- Hyperdrive: local installation, used for exam rooms when multiple people use the same computer > doesn't have to keep switching profiles, it's just local profiles

Client opens hyperspace > opens session on George's servers > connects to  Vir's web servers to use
- all of vir's servers are IIS

### Citrix
- Loadbalancing > citrix netscaler
### EPIC
- Offers great support and documentaiton
- Offers NOVA notes that offers details on new version of EPIC
	- release notes: do they want it , critical? > have meeting w/ representives from PAD, EMR, providers to get their input
- ECA - Epic Client Admins
	- Web server Admin - VIr
	- Hyperspace Admin - Groege
- Epic Print Service - everyone prints through this and Vir and search print jobs, print history > good for troubleshooting
- Epic Text - opens terminal > changes that haven't been migrated, mostly replaced by Kuiper


Use citrix to have a centralized place to update everything, part of EPIC

BCA (business continuity access) web doesn't run on Ctrix

Epic Satellite is a service that runs in the background of servers listening for commands sent by Kuiper or SystemPulse. This service runs on computers that communicate to Kuiper or SystemPulse (e.g. BCA computers)
2 kuiper servers
2 system pulse servers
### troubleshooting
sees a lot of data 
- Kuiper
- Citrix Director

vmware > hypervisor
- all servers run on this


there's a lot of redundancy > if they only need 2-3 servers to run, they have 4 servers
- System Pulse > monitoring


VIR DAY TO DAY
- Tenable Nessus (endpoint management)
- Checklists
- Support Logs (SLGs)
- Current Projects
	- Web BLOB storage
	- Citrix Netscaler ADC (Load balancer)

### Citrix Netscaler
- implement rate limiting
- in a high availability pair, but need to make something for DoS attacks
- 

KUIPER DASHBOARD

Servers
- BCA Web
- Epic Print Service
- Epic Care Link
- Hyperspace Web
- MyChart
- Interconnect Groups - All EPIC communication is going through this
	- BCA transfer, 

tiered storage based on interaction time, after certain amount of time, storage will get deleted on the storage but stay on the cloud

Audit
- third party
- pentesting and give them reports (RSM)


good summary:
tech support is the best :)