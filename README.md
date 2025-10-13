# Big Certificate 4 Project - Scope {Working Name}
## Team: Mitchell B, Liam D, Adam C, Bryce D
* Date Submitted: DD/MM/YYYY


#### 1. Project Objective / Main Scope:
* The objective of this team project is to conceptualize, develop, test, and deploy a network as per the requirements and network typology diagram. The project documentation will assist in the planning and initiation of the network prototype. The cybersecurity prototype model (CSOC) will be designed and produced for a small to medium sized organisation. 

* The project is to be completed in november 2025, with our aim for completion being mid to late november. The project will be completed alongside a presentation that will dicuss the process of planning, developing, and finalising of the cybersecurity model. The latest date we can complete the project is the 28th of November 2025.

* Success in this project is determined by the completion of the cybersecurity model. Our team will follow the Work Breakdown Structure and Gantt chart to complete each step of the process. By the end, the cybersecurity model should work without issue and comply with the requirements for the organisation.

***

#### 2. Project Deliverables:
| Deliverable No. | Description |
| -------- | ------- |
| 1. Documentaion | Provide clear documention for the planning of the cybersecurity model project. |
| 2. Gantt Chart | Provide a gantt chart that lists each step of the process with the estimated time frame for completing such step. |
| 3. Trello | Provide a trello board that displays the tasks under development and or completed. This will further back up the gantt chart and provide the client with a process of completion. |
| 4. Model Prototype | Provide a graphical prototype for the cybersecurity model typology inclduing all devices and connections. This will be produced in Cisco Packet Tracer. |
| 5. Meeting Minutes Reports | Provide reports of meetings discussing the project development. Meeting minutes provide a clear way of documenting the process of collaboration and planning. |
| 6. Completed cybersecurity Model | Provide the final completed cybersecurity model including all connections and configurations as planned during phase 2: Core Infrastructure Build and Configuration. |

***

#### 3. List of Project Tasks (Work Breakdown Structure)

1 Set up and interconnect networking infrastructure
   * 1.1 IP addresses
   * 1.2 Palo Alto Firewall – basic setup
   * 1.3 Palo Alto Firewall – basic feature configuration
       * 1.3.1 Static IP on Ethernet interface E1/1
       * 1.3.2 Zones
       * 1.3.3 Default static route in virtual router
       * 1.3.4 Device timezone
       * 1.3.5 Service routes
       * 1.3.6 Configure Source NAT from LAN to WAN (PAT)
       * 1.3.7 Configure base security policy: allow any from LAN to WAN
       * 1.3.8 Set up management profile to allow firewall management from host in internal network
   * 1.4 Switch SW1 – basic setup
       * 1.4.1 Clear switch config
       * 1.4.2 VLAN1 – 192.168.100.254/24 for remote management via SSH
       * 1.4.3 No port security at this stage
   * 1.5 Cable up physical network according to network diagram
   * 1.6 Palo Alto Firewall DHCP server
   * 1.7 Test PA firewall and switch
       * 1.7.1 Check PC Internet connectivity
       * 1.7.2 Telnet from your PC to the switch management IP
       * 1.7.3 Check you can manage the firewall from inside-management-profile
   * 1.8 Time estimate: 24 hours



2 Set up, configure and interconnect virtual environment, firewall, servers and client
   * 2.1 Install VirtualBox
   * 2.2 VirtualBox networking
       * 2.2.1 Set up a bridged network in VirtualBox for production VM installation – initial configuration
   * 2.3 Install Kali Purple
       * 2.3.1 Check IP and connectivity
       * 2.3.2 Update OS, services and apps from apt repository
       * 2.3.3 Set static IP
   * 2.4 Production network – connect Kali Purple to Palo Alto Firewall
   * 2.5 Install Windows 10/11 clients
   * 2.6 Install and configure Windows Server 2022 domain controller
       * 2.6.1 Install Server 2022
       * 2.6.2 Promote server to domain controller
       * 2.6.3 Create a security group and user accounts
       * 2.6.4 Join Windows clients to domain
       * 2.6.5 Set up DNS on domain controller
   * 2.7 Time estimate: 40 hours



3 Configure Kali Purple for remote management (SSH, RDP, console)
   * 3.1 Remote management configuration
   * 3.2 Time estimate: 8 hours



4 Implement Ubuntu Server Elastic Security SIEM (Elastic Stack: Elasticsearch, Kibana)
   * 4.1 Install Elasticsearch
   * 4.2 Convert to single-node setup (or replace FQDN in `initial_master_nodes` with IP address)
   * 4.3 Install Kibana
   * 4.4 Enrol Kibana
   * 4.5 Enable HTTPS for Kibana
       * 4.5.1 Generate required certificates and keys
   * 4.6 Create elastic user(s)
   * 4.7 Time estimate: 24 hours



5 Implement Fleet Server and endpoint protection (Elastic Defend)
   * 5.1 Overview and installation planning
   * 5.2 Fleet Server installation
       * 5.2.1 Install Fleet Server agent on Kali Purple
       * 5.2.2 (Option) Install Fleet Server to a central host
   * 5.3 Elastic Defend integration and Windows 10 endpoint agent
       * 5.3.1 Add Elastic Defend integration
       * 5.3.2 Install Elastic Agent on Windows host
       * 5.3.3 Confirm endpoint protection is configured in Windows client agent
   * 5.4 Configure an integration policy for Elastic Defend
       * 5.4.1 Policy settings
       * 5.4.2 Register Elastic Security as antivirus
   * 5.5 Set up security rules and alerts
       * 5.5.1 Rules
       * 5.5.2 Alerts
   * 5.6 Time estimate: 32 hours



6 Integrate OPNsense firewall logs with Kali Purple Elastic Security SIEM
   * 6.1 OPNsense → SIEM log integration
   * 6.2 Time estimate: 8 hours



7 Integrate Palo Alto Firewall with Kali Purple Elastic Security SIEM
  * 7.1 Palo Alto Firewall settings
       * 7.1.1 Timezone: Australia/Melbourne
       * 7.1.2 Latest AV, applications and threats database installed
   * 7.2 Create security policy – inside to outside allow
   * 7.3 Create source NAT policy – inside to outside
   * 7.4 Palo Alto Firewall syslog configuration
       * 7.4.1 Service route
       * 7.4.2 Syslog server profile
   * 7.5 Palo Alto Firewall Elastic integration
       * 7.5.1 Configure integration
   * 7.6 Confirm firewall is sending logs (Wireshark)
   * 7.7 Display firewall logs in Kibana
   * 7.8 Time estimate: 24 hours



8 DMZ Web server
   * 8.1 Set up DMZ web server in NAT network
   * 8.2 Set up DMZ web server virtual machine
   * 8.3 Update Ubuntu DMZ web server
   * 8.4 Configure DMZ web server for production network (Palo Alto Firewall)
       * 8.4.1 Bridge DMZ VM to Ethernet adapter on host
       * 8.4.2 PA FW – inside to DMZ security policy
       * 8.4.3 PA FW – DMZ to outside security policy
   * 8.5 PA FW – DMZ web server connectivity from Internet
       * 8.5.1 PA FW security policy – outside to DMZ web server
       * 8.5.2 PA FW NAT policy – destination NAT (outside → DMZ web server)
   * 8.6 Verify Ubuntu DMZ web server bridged to PA firewall
   * 8.7 DMZ web server connectivity to Kali Purple Elastic Security SIEM
   * 8.8 Install Elastic Defend agent in DMZ web server – production network
       * 8.8.1 Fleet agent policy – Linux server policy
       * 8.8.2 Install the agent on the Linux server via Linux tar script
       * 8.8.3 Confirm Linux DMZ server logs are successfully sent to Kibana
   * 8.9 DMZ web server remote management testing
       * 8.9.1 XRDP install
       * 8.9.2 SSH install
       * 8.9.3 Test remote management
   * 8.10 Time estimate: 40 hours



9 Configure and test network
   * 9.1 Configure and test domain user and computer accounts
   * 9.2 Configure and test domain group policies
   * 9.3 Configure and test elastic user accounts and roles
   * 9.4 Configure and test management VLAN / host isolation
   * 9.5 Configure and test domain DNS forwarding
   * 9.6 Time estimate: 24 hours



10 Establish a network security baseline
    * 10.1 Windows client application control
    * 10.2 Application patching
    * 10.3 Macro settings
    * 10.4 Application hardening
    * 10.5 Restrict admin privileges
    * 10.6 Patch operating systems
    * 10.7 MFA
    * 10.8 Regular backups
    * 10.9 Network segmentation and segregation
    * 10.10 Firewall security policies / profiles
    * 10.11 Time estimate: 32 hours



11 Testing / RBT activities
    * 11.1 Elastic Security alerts and rules
    * 11.2 Enumeration with Nmap scans
    * 11.3 Vulnerability scans
    * 11.4 Nikto web vulnerability scan
    * 11.5 Use OWASP ZAP
    * 11.6 Reporting
    * 11.7 Time estimate: 40 hours


***

#### 4. Project Costs
| Item | Cost ($) | Number needed | Total cost ($) |
| :---- | :---- | :---- | :---- |
| Firewall:  Palo alto 440 | 1400 | 1 | 1400 |
| Switch 48 port:  cisco 2960 | 6000 | 1 | 6000 |
| Switch 24 port: Cisco 2960 | 4200 | 1 | 4200 |
| Cables: Cat 5 | 7 per meter | 20m | 140 |
| Windows server: Server 2025 | 500 | 1 | 500 |
| Windows client: Windows 10 | 120 | 1 | 120 |
| Kali client:  | free | 1 | free |
| Kali server:  | 250 | 1 | 250 |
| Linux server:  | 250 | 1 | 250 |

The total cost of the items used is:  $ 12860

Staff cost

| Person | Cost per hour |
| :---- | :---- |
| Mitchell | $50 |
| Bryce | $50 |
| Adam | $50 |
| Liam | $50 |

***

#### 5. Project Risk Management
| Risk  | severity | How to mitigate |
| :---- | :---- | :---- |
| Electrocution | Moderate | Don’t stick anything metal into power outlets and if there is a power cable to hardware that looks damaged don’t use it and report it to someone so that they know and can fix it. |
| Tripping on cables | Moderate | Make sure that the cable management is there to make sure that the cables are out of the walk way. Watching where you step. |
| Training | Moderate | Make sure that all involved have the correct training and know what they need to in order to complete the task. |
| VMs crashing | High | Take regular snapshots and exports. |
| Sharp objects | High | Making sure that there aren't any wire prongs sticking out and are careful is metal on any of the hardware components. |
| Hardware failure| High | Regularly perform backups for data and implement a RAID system. |

__Mitigating existing risks__

Employing firewalls, encryption, multi-factor authentication, and intrusion detection systems to protect against cyber threats. <br>
Regularly updating and patching software to address known vulnerabilities and weaknesses.<br>
Establish a backup and recovery strategy to restore data in case of data loss or hardware loss.<br>
Continuously  monitor risk<br>

***

#### 6. Project Constraints
| Task No. | Description |
| -------- | ------- |
| Project Start Date | 2nd September 2025 |
| Launch / Go-Live Date | Late November 2025 |
| Project End Date | Late November 2025 |
| Hard Deadline | 28th November 2025 |
| Budget Constraints | {text here} |
| Quality / Performance Constraints | {text here} |
| Equipment / Personal Constraints | {text here} |
| Regulatory Constraints | {text here} |

***

#### 7. Updated Estimates
* 

***

#### 8. Approvals
* 

***