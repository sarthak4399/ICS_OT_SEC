# Introduction

## Overview

 Acomprehensive approach to securing Industrial Control Systems (ICS), taking into account their unique network, protocol, and application characteristics. It also considers various common compliance controls to offer practical guidance on implementing security measures in industrial environments.

## Key Concepts

- **Industrial Control Systems (ICS):** A broad term used to describe various control systems, including SCADA (Supervisory Control and Data Acquisition) and DCS (Distributed Control Systems).
- **OperatiIonal Technology (OT):** 

## Purpose
To bridge the gap between general enterprise security methods and the specific needs of industrial networks by providing:
- Deployment and configuration guidance
- Explanation of why certain security controls should be implemented
- Guidance on where and how these controls should be applied and used

## Goals
- Enhance the security of industrial networks by applying tailored security controls
- Provide practical, standards-based guidance for deployment and configuration
- Help readers understand the unique security requirements of ICS environments




ICS components interact within an industrial network in addition to knowledge of how industrial network protocols operate.
how control systems are connected
basic security flaws in an industrial network design

SYSTEM ASSETS:  PLC ,RTUs , IEDs,HMIs , workstations , servers data historians etc 

PLC : A programmable logic controller is a specialized industrial computer used to au- tomate functions within manufacturing facilities
PLCs were originally designed to replace electromechanical relays
control real-time processes,
plastic manufacturing, a catalyst may need to be injected into a vat when the temperature reaches a very specific value. If pro- cessing overhead or other latency introduces delay in the execution of the PLC’s logic
PLC logic programs :  IEC-61131-3 standerds 
Langauge : ladder logic , STL , FBD  ,Sequential Function Charts SFC
Image : from Images/Components of a programmable logic controller.
Protocols : PLCs can use a variety of digital and analog communications methods, but typi- cally use a fieldbus protocol, such as Modbus, ControlNet, EtherNet/IP, PROFIBUS,PROFINET

RTUs: REMOTE TERMINAL UNIT
 remote terminal unit typically resides in a substation, along a pipeline, or some other remote location. RTUs monitor field parameters and transmit that data back to a central monitoring station—typically either a master terminal unit (MTU) that may be an ICS server, a centrally located PLC, or directly to an HMI

 IEDs : RTUs and PLCs are designed for general use(i.e. they can be programmed to control the speed of a motor, to engage a lock, to activate a pump, or rail crossing gate)

 HUMAN–MACHINE INTERFACE : Human–machine interfaces are used as an operator’s means to interact with PLCs
HMI is software based
 Image : Images/Human–machine interface functionality.jpg

SYSTEM OPERATIONS:
industrial network protocols, devices, and topologies discussed are used to create and automate some industrial operation: refining crude oil, manufacturing a consumer product, purifying water, generating electricity, synthe- sizing and combining chemicals, and so on. A typical industrial operation consists of several layers of programmed logic designed to manipulate mechanical controls in order to automate the operation. Each specific function is automated by what is com- monly referred to as a control loop. Multiple control loops are typically combined or stacked together to automate larger processes.

CONTROL LOOPS: 
automated processes :- > Needs Control over the process 
these can be achive by various types of control systems , that is program with specific logic  . 
control action is necessary in order to perform a specific function

closed loop : output of the process affects the inputs
Open loop  : output of the process does not affects the inputs
images : Images/controllloop.jpg and complex_ctrl_loop.png


CONTROL PROCESSES: A “control process” is a general term used to define larger automated processes with- in an industrial operation. Many control processes may be required to manufacture a product or to generate electricity, and each control process may consist of one or many control loops.

FEEDBACK LOOPS:Every automated process relies on some degree of feedback both within a control loop and between a control loop or process and a human operator. Feedback is generally provided directly from the HMI used to control a specific process.


SAFETY INSTRUMENTED SYSTEMS: Safety instrumented systems (SIS) are deployed as part of a comprehensive risk man- agement strategy utilizing layers of protection to prevent a manufacturing environ- ment from reaching an unsafe operating condition. The basic process control system (BPCS) is responsible for discrete and continuous control necessary to operate a process within normal operational boundaries. In the event that an abnormal situa- tion occurs that places the processing outside of these normal limits, the SIS is pro- vided as an automated control environment that can detect and respond to the process event and maintain or migrate it to a “safe” state—typically resulting in equipment and plant shutdowns. As a final layer of protection, manufacturing facilities utilize significant physical protective devices including relief valves, rupture disks, flare systems, governors, and so on to act as a final level of safety prior to the plant enter- ing dangerous operating limits. These events and corresponding actions are shown in
Images : Layers of protection in plant safety design.png

Network toplogies : 
BUS , STAR , HYBRID , RING  MESH etc 

NETWORK SERVICES : IAM : directory servic- es, domain services, and others are required to ensure that all industrial zones have a baseline of access control in place.
WIreless Acess : Wireless
 networks might be required at almost any point within an industrial net- work, including plant networks, supervisory networks, process control networks, and field device networks. 
Remote Acesses: 

NETWORK SECURITY CONTROLS:Network security controls also introduce latency, typically to a greater degree than network switches and routers. This is because, as in switches and routers, every frame of network traffic must be read and parsed to a certain depth, in order to make decisions based upon the information available in Ethernet frame headers, IP packets headers, and payloads.
Hacking Industrial Control systems :Industrial networks are responsible for continuous and batch processing and other manufacturing operations.
Consequesse : Images/Consequences of a compromised industrial control system.png

Common Attecking suraface : 

Access Control 
Analyzers Managemet System 
Application Servers 
Assets management systems 
Controllers:(PLC RTUs MTUs)
User(ICS engineers , plant operators , technician )

COMMON ATTACK METHODS: MitM, Denial-of-Service (DoS), Replay attacks 

If an industrial network can be penetrated and malware deposited (on disk or in memory) anywhere on the network, tools such as Metasploit Meterpreter shell can be used to provide remote access to target systems, install keyloggers or keystroke injectors, enable local audio/video resources, manipulate control bits within industrial protocols, plus many other covert capabilities.
 exploitation of functionality versus the exploitation of vulnerabilities. In other words, issuing a “shutdown” command to a control device does not represent any particular weakness in the device per se. However, if the lack of authentication enables a malicious user to inject a shutdown command (i.e. perform a replay attack), this is a major vulnerability.

 MITM:A man-in-the-middle attack refers to an attack where the attacker goes between com- municating devices and snoops the traffic between them. The attacker is actually con- necting to both devices, and then relaying traffic between them so that it appears that they are communicating directly, even though they are really communicating through
 
 
a third device that is eavesdropping on the interaction
DENIAL-OF-SERVICE ATTACKS :DoS attacks in traditional business systems do not typically result in significant negative consequences if resolved in a timely manner. Access to a web page may be slowed, or email delivery delayed until the problem is resolved. How- ever, while there are rarely physical consequences associated with the interruption of services, a well-targeted DoS could bring very important systems off-line, and could even trigger a shutdown.

Replay attacks : Replay attacks are useful because of the command-and-control nature of an ICS. A replay attack can easily render a target system helpless because commands exist to enable or disable security, alarms, and logging features. Industrial proto- cols also enable the transmission of new programmable code (for device firmware and control logic updates)


Sophecticated attacks : spear phishing attack to access systems behind a fire- wall that would drop a remote access toolkit (RAT), and then obtain the credentials needed to access the trusted industrial networks, where targets may be compromised or exploited further.






INDUSTRIAL CYBER THREATS:
1982: First recorded ICS incident (Siberian pipeline sabotage).
2007: Stuxnet worm discovered, targeting Iran's nuclear facilities.
2013: Target data breach via compromised HVAC contractor.
2015: Ukrainian power grid attack causing widespread outages.
2017: WannaCry ransomware affects global industrial operations.
2021: Colonial Pipeline ransomware attack disrupts fuel supply.







 








