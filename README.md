# Cisco Packet Tracer: Inter-VLAN Routing (Legacy vs. Router-on-a-Stick)

## 🌐 Network Topology
[Inter-VLAN Routing Topology](ROS topology.png & legacy topology.png)

## 📝 Project Overview
This lab demonstrates how to enable communication between isolated VLANs (Inter-VLAN Routing) using two distinct methods: **Legacy Inter-VLAN Routing** and **Router-on-a-Stick (RoaS)**. 

The goal of this project is to understand the hardware efficiency and configuration differences between using physical interfaces versus logical subinterfaces.

## 🛠️ Concepts & Configurations Implemented

### 1. Legacy Inter-VLAN Routing
*   Configured separate physical router interfaces for each VLAN.
*   Connected each router port to a dedicated access port on the switch.
*   *Key takeaway:* Simple to configure, but highly inefficient as it wastes router ports.

### 2. Router-on-a-Stick (RoaS)
*   Configured a single physical router interface  divided into multiple logical **subinterfaces** (e.g., `fa0/0.1`, `fa0/0.2`).
*   Enabled **IEEE 802.1Q** encapsulation on each subinterface to match corresponding VLAN IDs.
*   Configured the connecting switchport as a **Trunk link** to carry tagged traffic to the router.
*   *Key takeaway:* Highly scalable and saves valuable physical router hardware.

## 🚀 How to Run the Lab
1. Download the `.pkt` file from this repository.
2. Open it in **Cisco Packet Tracer**.
3. Open a CLI terminal on any PC and run a `ping` command to a PC in a *different* VLAN to verify that the router is successfully forwarding Inter-VLAN traffic.
