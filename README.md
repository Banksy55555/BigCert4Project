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
| Task No. | Description |
| -------- | ------- |
| 1. Set up and interconnect networking infrastructure | 1.1 IP addresses
1.2 | Palo Alto Firewall – basic setup 1.3 Palo Alto Firewall – basic feature configuration
1.3.1 | Static IP on Ethernet interface E1/1
1.3.2 | Zones
1.3.3 | Default static route in virtual router
1.3.4 | Device timezone
1.3.5 | Service routes
1.3.6 | Configure Source NAT from LAN to WAN (PAT)
1.3.7 | Configure base security policy: allow any from LAN to WAN
1.3.8 | Set up management profile to allow firewall management from host in internal network
1.4 | Switch SW1 – basic setup
1.4.1 | Clear switch config
1.4.2 | VLAN1 – 192.168.100.254/24 for remote management via SSH
1.4.3 | No port security at this stage
1.5 | Cable up physical network according to network diagram
1.6 | Palo Alto Firewall DHCP server
1.7 | Test PA firewall and switch
1.7.1 | Check PC Internet connectivity
1.7.2 | Telnet from your PC to the switch management IP
1.7.3 | Check you can manage the firewall from inside-management-profile
1.8 | Time estimate: 24 hours |




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