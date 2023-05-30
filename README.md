# Realistic Network Intrusion Detection Evaluation Dataset for Federated Learning (FLNET2023) 

## Introduction

FLNET2023 is a state-of-the-art benchmark dataset for intrusion detection systems, specifically for Federated Learning applications. Generated using the CORE emulator, it embodies a realistic network topology and a diverse range of traffic and attack types. FLNET2023 aims to encourage robust research in federated learning based network intrusion detection.

### CORE Emulator 

 Common Open Research Emulator [CORE](https://github.com/coreemu/core) is a tool for emulating networks on one or more machines. You can connect these emulated networks to live networks. CORE consists of a GUI for drawing topologies of lightweight virtual machines, and Python modules for scripting network emulation.

### Network Topology

The dataset was generated based on the GEANT-2012 network topology, obtained from [The Internet Topology Zoo](http://www.topology-zoo.org/). This real-world topology represents a large-scale network infrastructure similar to those in Internet Service Providers (ISPs), with 40 nodes each representing primary routers serving specific locations or functions. The topology was replicated within the Common Open Research Emulator (CORE), where network traffic data was collected from ten strategically selected router nodes, labeled as {D1, D2, D3, ..., D10}, you can see in figure 1. These nodes cover different parts of the network and were chosen to provide a diverse and realistic data set.

### Network Traffic

FLNET2023 includes a broad mix of both normal and malicious network traffic, providing a realistic view of network interactions. The dataset spans over several kinds of common network protocols, like HTTP, TCP, UDP, and ICMP. 

### Labelled Dataset

Each instance in FLNET2023 is meticulously labeled, offering valuable information about the network flow it represents. The labels not only designate whether a given instance is normal or malicious but also provide specific details about the type of attack involved, if any. These labels significantly simplify the task of training and testing intrusion detection models.

### Atack diversity

The FLNET2023 dataset prominently features four types of DDoS attacks - DDoS-dyn, DDoS-stomp, DDoS-bot, and DDoS-tcp - commonly observed in real-world network scenarios. Acknowledging that threats within a network environment extend beyond DDoS, our dataset includes a variety of other attack types such as DoS-slowhttp and Infiltration-mitm. It also encompasses web-based attacks, including Command Injection, XSS, and SQL Injection. The inclusion of these diverse attack types enhances the realism of the dataset and ensures its alignment with actual network threat landscapes.

### Feature Set

The FLNET2023 dataset provides an extensive feature set, offering comprehensive details about each network flow. These features include source and destination IP addresses, port numbers, packet lengths, and timestamps, among others. This detailed feature set facilitates in-depth analysis and pattern recognition for intrusion detection models.

### MetaData

FLNET2023 includes rich metadata about each instance, which provides additional context and aids in data interpretation. The metadata includes details about the routers and their ip addresses which is crucial information for a comprehensive understanding of the dataset and for the effective development and evaluation of intrusion detection models.

### Data Collection Points 

The data points in the FLNET2023 dataset are collected from several unique nodes within the network topology, providing a well-rounded perspective of network activity. These collection points include various server nodes, and router nodes, each contributing to the dataset's diversity and depth. The collection points were selected with the intention of generating a dataset that reflects a broad range of network interactions. The IP address of the data collection points are given below in the table.

| Node | Interface |    IPv4     |
|------|-----------|-------------|
| D1   | eth0      | 10.0.48.2/24|
|      | eth1      | 10.0.49.1/24|
|      | eth2      | 10.0.50.1/24|
|      | eth3      | 10.0.51.1/24|
|      | eth4      | 10.0.52.1/24|
| D2   | eth0      | 10.0.29.1/24|
|      | eth1      | 10.0.30.2/24|
|      | eth2      | 10.0.56.2/24|
| D3   | eth0      | 10.0.22.2/24|
|      | eth1      | 10.0.23.1/24|
|      | eth2      | 10.0.38.1/24|
|      | eth3      | 10.0.40.2/24|
|      | eth4      | 10.0.45.2/24|
|      | eth5      | 10.0.47.2/24|
|      | eth6      | 10.0.43.1/24|
| D4   | eth0      | 10.0.1.2/24 |
|      | eth1      | 10.0.2.2/24 |
|      | eth2      | 10.0.5.2/24 |
|      | eth3      | 10.0.21.1/24|
|      | eth4      | 10.0.24.2/24|
|      | eth5      | 10.0.25.1/24|
| D5   | eth0      | 10.0.26.2/24|
|      | eth1      | 10.0.27.1/24|
|      | eth2      | 10.0.34.2/24|
|      | eth3      | 10.0.35.1/24|
| D6   | eth0      | 10.0.6.2/24 |
|      | eth1      | 10.0.7.1/24 |
|      | eth2      | 10.0.8.2/24 |
|      | eth3      | 10.0.35.2/24|
|      | eth4      | 10.0.54.2/24|
| D7   | eth0      | 10.0.53.2/24|
|      | eth1      | 10.0.54.1/24|
|      | eth2      | 10.0.55.1/24|
|      | eth3      | 10.0.56.1/24|
|      | eth4      | 10.0.57.2/24|
| D8   | eth0      | 10.0.8.2/24 |
|      | eth1      | 10.0.9.1/24 |
|      | eth2      | 10.0.55.2/24|
|      | eth3      | 10.0.60.2/24|
| D9   | eth0      | 10.0.9.2/24 |
|      | eth1      | 10.0.10.1/24|
|      | eth2      | 10.0.11.1/24|
|      | eth3      | 10.0.13.2/24|
|      | eth4      | 10.0.16.2/24|
| D10  | eth0      | 10.0.31.2/24|
|      | eth1      | 10.0.32.1/24|
|      | eth2      | 10.0.33.1/24|
|      | eth3      | 10.0.34.1/24|
|      | eth4      | 10.0.36.1/24|
|      | eth5      | 10.0.38.2/24|
|      | eth6      | 10.0.39.1/24|
|      | eth7      | 10.0.29.2/24|
|      | eth8      | 10.0.49.2/24|
|      | eth9      | 10.0.53.1/24|

### Other Router Nodes

In addition to the data collection points, FLNET2023 incorporates a multitude of other router nodes, enhancing the realism and complexity of the network topology. These router nodes play pivotal roles in directing network traffic and simulating real-world network congestion and routing scenarios. Their inclusion in the topology helps portray a more authentic network environment and induces additional challenges for intrusion detection. The IP address of the other router nodes are given below in the table.

| Node | Interface |    IPv4     |
|------|-----------|-------------|
| R1   | eth0      | 10.0.46.1/24|
| R2   | eth0      | 10.0.45.1/24|
|      | eth1      | 10.0.59.1/24|
|      | eth2      | 10.0.46.2/24|
| R3   | eth0      | 10.0.47.1/24|
|      | eth1      | 10.0.59.2/24|
| R4   | eth0      | 10.0.58.2/24|
|      | eth1      | 10.0.44.1/24|
| R5   | eth0      | 10.0.43.2/24|
|      | eth1      | 10.0.58.1/24|
| R6   | eth0      | 10.0.42.2/24|
|      | eth1      | 10.0.44.2/24|
|      | eth2      | 10.0.48.1/24|
| R7   | eth0      | 10.0.41.1/24|
|      | eth1      | 10.0.42.1/24|
| R8   | eth0      | 10.0.39.2/24|
|      | eth1      | 10.0.40.1/24|
| R9   | eth0      | 10.0.21.2/24|
|      | eth1      | 10.0.22.1/24|
| R10  | eth0      | 10.0.23.2/24|
|      | eth1      | 10.0.24.1/24|
|      | eth2      | 10.0.36.2/24|
|      | eth3      | 10.0.37.2/24|
| R11  | eth0      | 10.0.0.1/24 |
|      | eth1      | 10.0.37.1/24|
| R12  | eth0      | 10.0.0.2/24 |
|      | eth1      | 10.0.1.1/24 |
| R13  | eth0      | 10.0.25.2/24|
|      | eth1      | 10.0.32.2/24|
| R14  | eth0      | 10.0.28.1/24|
|      | eth1      | 10.0.33.2/24|
| R15  | eth0      | 10.0.2.1/24 |
|      | eth1      | 10.0.3.1/24 |
|      | eth2      | 10.0.27.2/24|
|      | eth3      | 10.0.28.2/24|
| R16  | eth0      | 10.0.4.2/24 |
|      | eth1      | 10.0.5.1/24 |
| R17  | eth0      | 10.0.3.2/24 |
|      | eth1      | 10.0.4.1/24 |
|      | eth2      | 10.0.6.1/24 |
|      | eth3      | 10.0.26.1/24|
| R18  | eth0      | 10.0.7.2/24 |
|      | eth1      | 10.0.60.1/24|
| R19  | eth0      | 10.0.10.2/24|
| R20  | eth0      | 10.0.11.2/24|
|      | eth1      | 10.0.12.1/24|
| R21  | eth0      | 10.0.12.2/24|
|      | eth1      | 10.0.13.1/24|
|      | eth2      | 10.0.14.1/24|
|      | eth3      | 10.0.15.1/24|
| R22  | eth0      | 10.0.14.2/24|
| R23  | eth0      | 10.0.15.2/24|
|      | eth1      | 10.0.16.1/24|
|      | eth2      | 10.0.17.1/24|
|      | eth3      | 10.0.18.1/24|
|      | eth4      | 10.0.29.2/24|
| R24  | eth0      | 10.0.17.2/24|
| R25  | eth0      | 10.0.20.2/24|
|      | eth1      | 10.0.57.1/24|
| R26  | eth0      | 10.0.18.2/24|
|      | eth1      | 10.0.19.1/24|
|      | eth2      | 10.0.20.1/24|
| R27  | eth0      | 10.0.19.2/24|
| R28  | eth0      | 10.0.30.1/24|
|      | eth1      | 10.0.31.1/24|
|      | eth2      | 10.0.50.2/24|
| R29  | eth0      | 10.0.52.2/24|
| R30  | eth0      | 10.0.51.2/24|


## Dataset URL

## License 

The FLNET2023 dataset consists of labeled network flowsincluding full packet payload in pcap format. It is publicly available for researchers to facilitate further advancements in the field of intrusion detection.