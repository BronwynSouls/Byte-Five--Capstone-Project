IT INFRASTRUCTURE AND SUPPORT CAPSTONE PROJECT
Design and Implementation of an IT Infrastructure and Support Solution
Final Capstone Report
Company:  Ubuntu Innovations (Pty) Ltd
Location:  Cape Town, South Africa
Number of employees:  25
Prepared by:  The Byte 5
Programme:  CAPACITI · IT Support Capstone
Date:  October 2026
Team members: Thapelo Moncho, Bronwyn Souls, Simphiwe Thwabuse, Emaad Mentor, Khanya Gusha

If the table above is empty, right-click it in Word and choose Update Field.
Executive Summary
Ubuntu Innovations (Pty) Ltd is a fast-growing technology startup in Cape Town, South Africa. As the company relocates to a new office, it needs a reliable and secure IT infrastructure to support its 25 employees across five departments and its daily operations.
This report presents the complete IT infrastructure and support solution designed by The Byte 5. It analyses the company's business and technical requirements and recommends the hardware, software and network design needed to meet them. It then sets out an IP addressing plan using VLANs, a department-based user and permissions model, operating system administration procedures, a 3-2-1 backup and disaster recovery plan, a cybersecurity policy, a risk assessment, an incident response plan and a troubleshooting guide. The report closes with the team's career readiness materials, conclusions and recommendations.
The proposed infrastructure aims to ensure:
•	Stable wired and wireless network connectivity with room for growth
•	Secure, role-based access to company resources
•	Effective communication and collaboration
•	Data protection through encryption, backups and tested recovery
•	Efficient, documented IT support for all employees and departments
Key recommendations include a business-grade router/firewall and 24-port managed switch, six VLANs on the 192.168.0.0/16 private range, an 8TB RAID NAS for central storage, UPS protection against load shedding, mandatory multi-factor authentication, full-disk encryption, managed endpoint detection and response, and regular restore testing.
Business Requirements Analysis
Company Overview
Ubuntu Innovations (Pty) Ltd is a technology startup operating in Cape Town, South Africa. The company is experiencing growth and is relocating to a new office. The new office requires an IT environment that can support daily business operations while providing adequate security, reliability, scalability and data protection.
Organisational Structure
The company has 25 employees distributed across five departments.
Department	Employees	Key IT needs
Executive Management	3	Office applications, email, video conferencing, business reporting tools
Finance	4	Spreadsheets, accounting/financial software, banking platforms, secure document storage
Human Resources	3	HR management software, word processing, spreadsheets, employee records management
Sales and Marketing	7	CRM software, email, marketing tools, presentation software, web browsers
Software Development	8	IDEs, Git, GitHub, programming languages and frameworks, database and collaboration tools
Total	25	
Table 1: Departments, staff numbers and IT needs
Business Applications Required
Employees will require different applications depending on their roles. All employees may require:
•	Email and communication tools
•	Web browsers
•	Word processing, spreadsheet and presentation software
•	PDF reader
•	Video conferencing software
•	Antivirus/endpoint security software
•	Cloud storage or file-sharing tools
Department-specific applications are listed in Table 1 and in the Hardware and Software Inventory section.
Data Security Requirements
Because the company will store business and potentially sensitive employee and financial information, security must be considered from the beginning. The infrastructure should include:
•	Strong passwords and user authentication
•	Access control and restricted access to sensitive folders
•	Antivirus/endpoint protection
•	Regular software updates
•	Firewall protection
•	Data backups
•	Secure Wi-Fi
Finance and HR information should not be accessible to employees who do not require it for their jobs.
Connectivity Needs
Ubuntu Innovations requires reliable wired and wireless connectivity. The infrastructure should provide:
•	Reliable internet access
•	Wired connections for desktop computers
•	Wireless access for laptops and mobile devices
•	Network access for printers and the NAS storage device
•	Secure internal communication between devices
•	Sufficient network capacity for 25 employees, with room for future growth
A business-grade router/firewall and managed switch are recommended to provide reliable connectivity and improved network management.
Operational Challenges
The company may experience several IT-related challenges, including internet connection failures, hardware failures, printer problems, power outages (including load shedding), cybersecurity attacks, malware infections, accidental deletion of files, unauthorised access, data loss and software failures. The infrastructure must therefore be designed with reliability, security and recovery in mind.
Hardware and Software Inventory
Hardware Inventory
To support Ubuntu Innovations' operations, the company requires a mix of desktop computers, laptops, networking equipment, storage and power protection devices.
Device	Qty	Specification	Purpose
Desktop computers	20	Intel Core i5, 16GB RAM, 512GB SSD	Day-to-day office work and multitasking
Laptops	5	Intel Core i7, 16GB RAM, 512GB SSD, Wi-Fi 6, webcam	Management and employees who need mobility
Router/firewall	1	Business-grade	Internet connectivity, network security, traffic management and firewall protection
Managed switch	1	24-port Gigabit	Connects all wired devices; enables monitoring and control
Wireless access points	2	Wi-Fi 6	Secure, reliable wireless coverage throughout the office
Network printers	2	Laser	Shared across departments, reducing printing costs and maintenance
NAS device	1	8TB RAID storage	Centralised file sharing, document storage and backups
UPS devices	2	1500VA	Protects critical equipment from power outages, data loss and electrical problems
Table 2: Hardware inventory
This hardware provides employees with reliable computing resources, secure connectivity, centralised data storage, efficient printing services and protection against power interruptions.
Standard Software for All Employees
Software category	Recommended software	Purpose
Operating system	Ubuntu LTS or approved business operating system	Stable and secure computing platform
Web browser	Firefox or Google Chrome	Internet and web applications
Office productivity	LibreOffice or Microsoft 365	Documents, spreadsheets and presentations
PDF reader	Built-in PDF reader	Viewing business documents
Communication	Microsoft Teams, Zoom or approved platform	Meetings and collaboration
Security software	Endpoint protection and antivirus	Malware and threat protection
Backup client	Approved NAS or cloud backup client	Data protection
Password manager	Company-approved password manager	Secure password storage
Compression utility	7-Zip or built-in archive tool	Managing compressed files
Table 3: Standard software
Department-Specific Software
Department	Required software
Executive Management	Office applications, video conferencing, financial dashboards, document signing tools
Finance	Spreadsheet software, accounting software, payroll applications, PDF tools
Human Resources	HR management system, document management software, recruitment platforms
Sales and Marketing	CRM software, email marketing tools, presentation software, design tools
Software Development	Visual Studio Code, Git, GitHub access, programming languages, Docker, testing tools
IT Support	Remote support tools, monitoring tools, ticketing system, network diagnostic tools
Table 4: Department-specific software
Licensing Requirements
All software should be legally licensed and maintained according to the company's licensing requirements. The company must:
•	Maintain a software licensing register
•	Purchase enough licences for all users
•	Avoid installing unauthorised or pirated software
•	Track licence expiry dates
•	Remove software when it is no longer required
•	Review software usage to control costs
•	Keep proof of purchase and licence agreements
Network Design
The proposed network uses a central router/firewall and managed switch. The ISP provides the internet connection to the office. The connection is passed to the router/firewall, which provides security and routing between the internet and the internal network. The managed switch provides wired connectivity to desktop computers, printers, NAS storage and the wireless access points.
 
Figure 1: Network topology
Network Components
Component	Role
ISP	Supplies the company's internet connection
Router/firewall	Connects the internal network to the internet and provides security controls
Managed switch	Connects the company's wired devices and supports VLANs
Wireless access points (2)	Provide wireless connectivity throughout the office
Desktop computers (20)	Workstations for employees
Laptops (5)	Mobility, particularly for management and employees requiring flexible working
Network printers (2)	Shared by authorised employees over the network
NAS	Centralised file storage and backup capabilities
Table 5: Network components
IP Addressing Plan
The office network uses the private address range 192.168.0.0/16, divided into VLANs to improve security, performance and management. Each subnet is a /24 providing usable addresses from .1 to .254.
Network Segments (VLANs)
VLAN	Segment	Subnet	Gateway
10	Management	192.168.10.0/24	192.168.10.1
20	Servers / NAS	192.168.20.0/24	192.168.20.1
30	User devices	192.168.30.0/24	192.168.30.1
40	Printers	192.168.40.0/24	192.168.40.1
50	Staff Wi-Fi	192.168.50.0/24	192.168.50.1
60	Guest Wi-Fi	192.168.60.0/24	192.168.60.1
Table 6: VLAN and subnet allocation
Static IP Assignments
Infrastructure devices use fixed IP addresses.
Device	IP address
Router	192.168.10.1
Managed switch	192.168.10.2
Wireless access points	192.168.10.3 – 192.168.10.4
NAS device	192.168.20.10
Network printers	192.168.40.10 – 192.168.40.11
Table 7: Static IP assignments
DHCP Ranges
Segment	DHCP range
User devices	192.168.30.100 – 192.168.30.240
Staff Wi-Fi	192.168.50.100 – 192.168.50.240
Guest Wi-Fi	192.168.60.100 – 192.168.60.240
Table 8: DHCP ranges
An example user device configuration is provided in Appendix B. Staff Wi-Fi uses WPA2-Enterprise or WPA3-Enterprise.
Main Security Rules
•	Guest Wi-Fi must not access company servers or internal devices.
•	Only IT administrators may access the management VLAN.
•	User devices must not directly access management devices.
•	Printers should be isolated from unnecessary traffic.
•	Firewalls must control communication between VLANs.
•	Wireless passwords must remain private.
•	Network equipment must use strong passwords and multi-factor authentication where available.
User and Permissions Matrix
The company uses department-based security groups. Users are added to the group that matches their department, and access is granted to folders through these groups instead of assigning permissions to individual users.
Security Groups
Department	Security group	Folder access
Management	mgmt_grp	Full access
Finance	finance_grp	Finance + Public
Human Resources	hr_grp	HR + Public
Sales and Marketing	sales_grp	Sales + Public
Software Development	dev_grp	Development + Public
Table 9: Department security groups
Folder Access Matrix
Folder	mgmt_grp	finance_grp	hr_grp	sales_grp	dev_grp
Public	Read/Write	Read/Write	Read/Write	Read/Write	Read/Write
Management	Full	No access	No access	No access	No access
Finance	Full	Read/Write	No access	No access	No access
HR	Full	No access	Read/Write	No access	No access
Sales	Full	No access	No access	Read/Write	No access
Development	Full	No access	No access	No access	Read/Write
Table 10: Folder access matrix (shared folders on the NAS; see Appendix A)
Permission Principles
•	Users receive only the access required for their job (least privilege).
•	Department folders are accessible only to the relevant department.
•	IT administrators manage permissions but should not access confidential files unless authorised.
•	Former employees must have their accounts disabled immediately.
•	Shared accounts must not be used.
•	Permissions must be reviewed every three months.
•	Management approval is required before granting access to confidential folders.
Operating System Administration
User and Group Administration
Each employee receives an individual account and is added to their department's security group. New hires join a group, staff who change roles move to a different group, and leavers' accounts are disabled immediately. This avoids folder-by-folder permission changes and keeps access auditable.
Command-Line Administration Guide
The command-line administration guide is maintained in the team's GitHub repository. It demonstrates the folder and permission setup on Linux using commands such as mkdir, chown and chmod. Repository: BronwynSouls/Byte-Five--Capstone-Project
Software Deployment Process
1.	Confirm that the software is approved by management.
2.	Verify licensing and subscription requirements.
3.	Check that the software is compatible with the operating system.
4.	Test the software on a non-production device.
5.	Back up the user's important data.
6.	Install the software.
7.	Apply current updates and security patches.
8.	Configure the software according to company standards.
9.	Test the application with the user.
10.	Record the installation in the software inventory.
Update Management
•	Critical security updates should be installed as soon as possible after testing.
•	Standard updates should be installed during scheduled maintenance periods.
•	Operating system updates should be centrally monitored where possible.
•	Users should not disable security updates.
•	Failed updates must be recorded and investigated.
•	Systems should be restarted when required to complete updates.
The monthly patch cycle is described in the Cybersecurity Policy section.
Backup and Recovery Plan
Backup Strategy: The 3-2-1 Rule
Rule	Implementation
3 copies	All business data: the live data plus two backups
2 storage media	On-site NAS and cloud storage
1 copy offsite	Encrypted and immutable (cannot be changed or deleted), protecting against fire, theft and ransomware
Table 11: 3-2-1 backup strategy
Data in Scope
•	Departmental shared folders on the file server/NAS (Executive, Finance, HR, Sales and Marketing, Software Development)
•	Finance and payroll system databases
•	Directory services data (user accounts, groups and Group Policy)
•	Email and cloud productivity data (Microsoft 365 or Google Workspace, using a third-party backup service)
•	Source code: GitHub remote repositories plus a nightly mirror to the NAS
•	Server and network device configurations (firewall, switches, wireless access points)
Not backed up centrally: local laptop drives. Staff must save work to approved shared folders or synced company cloud storage. Laptops are rebuilt from a standard image if they fail.
Backup Schedule and Retention
Backup type	Frequency	Description	Rentation 
Incremental	Daily	Copies only files changed since the previous backup; fast and small	14 days 
Full	Weekly	Copies everything and forms the base for restores	4 Weeks 
Archive	Monthly	Long-term history for audits and recovering files deleted long ago	12 Months or longer 
Table 12: Backup schedule
Security, Monitoring and Testing
•	Encryption: AES-256 at rest and TLS in transit for all backups.
•	Monitoring: backup success/failure reports are emailed to IT daily; failed jobs are investigated and re-run the same day.
•	Restore testing: a test restore of a random folder monthly, and a full disaster recovery test every six months.
•	Data residency: a South African cloud region supports compliance with POPIA.
•	Access control: backup consoles are limited to IT administrators and protected with MFA.
Recovery Objectives (RTO and RPO)
Recovery Time Objective (RTO): the maximum acceptable time a system can be down before it must be restored.
Recovery Point Objective (RPO): the maximum acceptable amount of data loss, measured backwards from the time of the incident.
Priority	Systems	RTO	RPO
Critical	Core business apps, databases, authentication (e.g., Active Directory), email, payment/transaction systems	1 hour or less	15 minutes or less
Important	File servers, internal apps, CRM, collaboration tools	4 to 8 hours	4 to 12 hours
Standard	Archives, test/dev environments, non-essential workstations, reporting tools	24 to 72 hours	24 hours
Table 13: Recovery objectives (targets to be completed by the team)
Cloud-hosted email and GitHub repositories have near-zero RPO because the provider stores data continuously; our backups protect against accidental deletion, account compromise and ransomware.
Disaster Recovery Procedure
1.	Declare: the IT Support Lead assesses the impact and declares a disaster together with the COO.
2.	Communicate: notify staff through the emergency WhatsApp group or SMS and set expectations.
3.	Prioritise: restore Critical systems first, then Important, then Standard.
4.	Restore: recover from the latest clean backup: the NAS first, or the cloud if the NAS is lost.
5.	Verify: department heads confirm data integrity and that users can access their systems.
6.	Document: record the timeline, any gaps, and the actual RTO/RPO achieved.
Site Loss Scenario
If the office becomes unusable (fire, flood or a prolonged outage), staff will work remotely on their laptops. Critical services will be restored from the Cape Town cloud region to temporary cloud servers. An offsite recovery kit (encryption keys, emergency admin credentials in a sealed vault, and vendor contact details) is held by the CEO and the IT Support Lead.
Cybersecurity Policy
Purpose and Scope
This policy protects the confidentiality, integrity and availability of Ubuntu Innovations' information. It applies to all employees, contractors and interns, and to every company device, account and system, including personal devices used for work.
Password Complexity Requirements
•	Minimum 12 characters for user accounts and 16 characters for administrator accounts.
•	Passphrases are encouraged (for example, four random words). Passwords must mix upper- and lower-case letters with numbers or symbols.
•	The last 10 passwords may not be reused; passwords must not contain the company name or personal information.
•	Accounts lock for 15 minutes after 5 failed login attempts.
•	Passwords must be changed immediately if compromise is suspected; administrator passwords are changed every 90 days.
•	All work credentials are stored in the company password manager (e.g. Bitwarden). Passwords must never be written down or shared.
Multi-Factor Authentication (MFA)
•	MFA is mandatory for email, cloud applications, VPN/remote access and all administrator accounts.
•	The preferred method is an authenticator app (push notification or code). SMS is used only as a fallback.
•	Hardware security keys (FIDO2) are required for IT administrators, executives and the Finance team.
•	MFA resets require identity verification by video call or in person.
•	Users must never approve an MFA prompt they did not initiate, and must report unexpected prompts to IT immediately.
Device Encryption
•	Full-disk encryption is required on every laptop and desktop: BitLocker (Windows), FileVault (macOS) and LUKS (Ubuntu developer machines).
•	Encryption recovery keys are stored centrally in the directory service, never on the device itself.
•	Company mobile phones must be encrypted and enrolled in Mobile Device Management (MDM) with remote wipe enabled.
•	Only encrypted USB drives may be used to store company data.
•	Wireless networks use WPA2/WPA3-Enterprise, and all web applications use HTTPS/TLS.
Antivirus and Endpoint Security Standards
•	A centrally managed endpoint detection and response (EDR) solution (e.g. Microsoft Defender for Business) is installed on all devices.
•	Real-time protection is always on; users cannot disable it.
•	Malware definitions update at least daily, and a full scan runs weekly.
•	Alerts reach IT within 15 minutes; infected devices are automatically isolated from the network.
•	IT produces a monthly report on device health and non-compliant endpoints.
Patch Management
1.	Identify: monthly review after Microsoft Patch Tuesday, plus vendor and Ubuntu security notices.
2.	Test: deploy to a pilot group (IT plus two users per department) for 48 hours.
3.	Deploy: automatic rollout using WSUS/Intune for Windows and unattended-upgrades for Ubuntu.
4.	Verify: run a compliance report and follow up on devices that missed updates.
Scope includes operating systems, browsers, office software, third-party applications, the NAS, printers, and firewall/router/switch firmware (reviewed quarterly). Unsupported (end-of-life) software is replaced, not kept.
Acceptable Use Policy
Employees must:
•	Use company systems mainly for business purposes; limited, reasonable personal use is allowed.
•	Lock their screen when stepping away (Windows+L); screens auto-lock after 5 minutes.
•	Store work files only in approved shared folders or company cloud storage.
•	Handle personal information in line with POPIA.
•	Report lost or stolen devices to IT within 1 hour.
Employees must not:
•	Share passwords or allow others to use their account.
•	Install unlicensed or unapproved software.
•	Disable antivirus, firewalls or encryption.
•	Use personal cloud storage or personal USB drives for company data.
•	Access, store or send illegal, offensive or harassing content.
Monitoring and enforcement: company systems may be monitored for security purposes. Breaches of this policy may lead to disciplinary action in line with HR procedures. Every employee signs this policy during onboarding, before receiving system access.
Security Awareness Training
People are the first line of defence. This short, practical programme trains all 25 employees in about 2.5 hours in total.
Training modules: Refer to Excell 
Role-specific add-ons:
•	Finance: payment verification procedures and business email compromise.
•	Software Development: secure coding, secrets management, and protecting GitHub access.
•	Executive Management: targeted ("whaling") attacks aimed at senior staff.
Delivery schedule:
•	Onboarding: all modules completed in the first week; the Acceptable Use Policy is signed before system access is granted.
•	Annual refresher: updated with recent incidents and new threats.
•	Quarterly phishing simulations: safe test emails, with extra coaching for anyone who clicks.
•	Monthly micro-tips: a five-minute tip in team meetings or on Slack/Teams.
Risk Assessment
Each risk is rated High, Medium or Low for likelihood (how probable it is) and impact (how much damage it would cause). Mitigations reduce either the likelihood, the impact, or both.
Risk	Likelihood	Impact	Risk level	Mitigation
Phishing	High	High	High	Awareness training, phishing simulations, MFA, payment verification
Power outage / load shedding	High	High	High	UPS (and inverter) for core network and NAS
Internet failure	Medium	High	High	ISP support; remote/cloud fallback
Hardware failure	Medium	High	High	Spares, warranties, standard device image
Malware / ransomware	Medium	High	High	Managed EDR, patching, immutable offsite backups
Data loss	Medium	High	High	3-2-1 backups with monthly restore tests
Unauthorised access	Medium	High	High	Group-based access control, MFA, quarterly reviews
Accidental deletion	Medium	High	High	Daily backups and file restore
Switch failure	Low/Medium	High	Medium/High	Replacement planning
Printer failure	Medium	Medium	Medium	Two shared printers
Software failure	Medium	Medium	Medium	Updates, testing and recovery
Table 14: Risk assessment matrix
Top Priorities
•	Phishing: the highest combined rating; the Finance team is a likely target for fake invoice and payment-change scams.
•	Ransomware and unpatched software: could stop work for all 25 employees; reliable backups are the last line of defence.
•	Load shedding: frequent in South Africa; a UPS and inverter keep the core network and server running.
Incident Response Plan
A security incident is any event that threatens the confidentiality, integrity or availability of company information, for example a malware infection, a compromised account, a lost laptop or a data leak. This plan ensures every incident is handled in the same, repeatable way.
Severity Levels
Incidents are assigned a severity level during triage. P1 incidents are the most serious and are escalated to management within 1 hour
The Six Phases
1.	Detection. Incidents are identified through EDR alerts, firewall and login logs, backup failures, or reports from employees. IT triages each event and assigns a severity level.
2.	Reporting. Employees report suspected incidents to the IT helpdesk within 15 minutes by phone, email or ticket. IT escalates P1 incidents to management within 1 hour. All actions are recorded in an incident log.
3.	Containment. Limit the damage: isolate affected devices from the network, disable compromised accounts, block malicious senders or IP addresses, and preserve evidence (logs, screenshots) before making changes.
4.	Eradication. Remove the cause: delete malware, re-image infected devices, reset passwords and MFA, and patch the vulnerability that was exploited.
5.	Recovery. Restore systems and data from clean backups, confirm with users that everything works, and monitor closely for two weeks for signs of reinfection.
6.	Lessons learned. Hold a no-blame post-incident review within 5 working days. Update policies, training and security controls based on what was learned.
Roles and Responsibilities
The IT Support Lead, the COO and the CEO hold key roles in disaster and incident decisions.
Legal and External Notification
•	If personal information is compromised, the Information Regulator and affected people must be notified as soon as reasonably possible, as required by section 22 of POPIA.
•	Criminal incidents are reported to the South African Police Service (SAPS) and the case number is recorded.
•	For P1 incidents, the cyber insurer (if applicable) and an external security partner are contacted.
Troubleshooting Guide
Every support case follows the same method: check the simple things first, isolate the cause, fix it, test it and document the outcome. If a problem cannot be resolved, it is documented and escalated.
Scenario 1: Desktop Will Not Turn On
Common causes:
•	Loose or faulty power cable
•	Faulty power outlet or UPS
•	Failed power supply
•	Hardware or power button problem
Steps:
1.	Check the power cable and outlet.
2.	Make sure the UPS is switched on.
3.	Test the outlet with another device.
4.	If possible, try another power cable.
5.	Check for power lights or fan activity.
6.	If it still does not start, report the problem for repair.
Resolution: The power cable was loose. Reconnecting it fixed the problem.
Scenario 2: No Internet
Common causes:
•	Disconnected Ethernet cable or Wi-Fi
•	Disabled network adapter
•	Incorrect network settings
•	Router, switch, DNS or ISP problem
Steps:
1.	Check the Ethernet cable or Wi-Fi.
2.	Check the computer's network status.
3.	Ask whether other employees have internet access.
4.	Test the network connection.
5.	Restart the connection if necessary.
6.	Check the router or switch.
7.	Contact the ISP if the whole office is affected.
Resolution: The Ethernet cable was disconnected. Reconnecting it restored internet access.
Scenario 3: Printer Offline
Common causes:
•	Printer switched off
•	Disconnected network cable
•	Paper jam or low toner
•	Print queue or driver problem
•	Network or IP address issue
Steps:
1.	Make sure the printer is switched on.
2.	Check for error messages, paper and toner.
3.	Check the network cable.
4.	Ask whether other users can print.
5.	Clear stuck print jobs.
6.	Restart the printer if needed.
7.	Print a test page.
Resolution: The printer's network cable was disconnected. Reconnecting it brought the printer back online.
Career Readiness Materials
The final week turned the technical work into career materials. Each team member prepared:
Output	Description
IT Support CV	One page, built around skills proven in this capstone
Cover letter	Tailored to a specific IT support role and employer
LinkedIn summary	A professional profile that links to the project portfolio
Interview preparation	10 IT support interview questions with structured sample answers
Table 15: Career readiness outputs
This capstone gives the team concrete evidence to discuss with employers: a VLAN-based network design, a group-based permissions model, a 3-2-1 backup plan and a full cybersecurity policy.
AI tools were used to identify transferable skills, tailor applications, plan and track the job search, and practise mock interviews. Every output was reviewed and edited by the team so that it is accurate and sounds like us.
Conclusion and Recommendations
Conclusion
The proposed solution gives Ubuntu Innovations a secure, reliable and documented IT environment for its new Cape Town office. Business-grade networking, VLAN segmentation and UPS protection keep the office connected; group-based permissions and a layered cybersecurity policy protect company and personal information; and a tested 3-2-1 backup plan, incident response plan and troubleshooting guide ensure the company can recover from failures and support its staff efficiently.
Key Lessons Learned
1.	Security is designed in: VLANs, MFA and encryption are far easier to plan from day one than to retrofit.
2.	Groups scale, individuals don't: department groups keep access simple, auditable and quick to change.
3.	A backup counts once restored: regular restore tests prove the plan works before a real disaster does.
4.	Documentation is part of the fix: clear, repeatable steps let the next technician pick up where we left off.
Recommendations
•	Deploy the recommended hardware, VLAN design and static/DHCP addressing before staff move into the new office.
•	Enforce MFA, full-disk encryption and managed EDR on all devices from the first day.
•	Run monthly restore tests and a full disaster recovery test every six months.
•	Deliver the security awareness programme at onboarding, with quarterly phishing simulations.
•	Review user permissions every three months and disable leavers' accounts immediately.
•	Maintain the software licensing register and follow the monthly patch cycle.
•	Keep this documentation updated as the company grows beyond 25 users.
References
Republic of South Africa (2013) Protection of Personal Information Act 4 of 2013 (POPIA). Pretoria: Government Gazette.
Rekhter, Y. et al. (1996) RFC 1918: Address Allocation for Private Internets. Internet Engineering Task Force. Available at: https://www.rfc-editor.org/rfc/rfc1918
course references:
Google IT Support Professional Certificate — Coursera
Technical Support Fundamentals
The Bits and Bytes of Computer Networking
Operating Systems and You
System Administration and IT Infrastructure Services
IT Security: Defense against the Digital Dark Arts

Appendices
Appendix A: Shared Folder Structure
Shared files are stored on the company NAS device or file server.
/UBUNTU
├── Public
├── Management
├── Finance
├── HR
├── Sales
└── Development

Appendix B: Example Network Settings
Setting	Value
IP address	192.168.30.101
Subnet mask	255.255.255.0
Default gateway	192.168.30.1
DNS	Internal DNS or an approved public DNS
DHCP	Enabled for user devices
Wi-Fi security	WPA2-Enterprise or WPA3-Enterprise
Table 16: Example user device configuration
Appendix C: Command-Line Administration Guide
The full command-line administration guide is available in the team's GitHub repository:
