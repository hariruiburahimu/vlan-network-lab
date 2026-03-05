# VLAN Network Lab

This project demonstrates basic VLAN configuration and network segmentation using a Layer 2 switch in Cisco Packet Tracer.

## Overview

Virtual LANs (VLANs) allow network administrators to segment a physical network into multiple logical networks. Devices in different VLANs cannot communicate without routing.

This lab demonstrates how VLANs isolate traffic within the same switch.

## Topology

- 4 PCs
- 1 Switch (Cisco 2960)

Two VLANs are created:

- VLAN 10 — Sales
- VLAN 20 — IT

Devices in the same VLAN can communicate, while devices in different VLANs cannot.

## Configuration Steps

1. Assign IP addresses to the PCs
2. Create VLANs on the switch
3. Assign switch ports to VLANs
4. Test connectivity using ping

## Expected Results

- Communication works between devices in the same VLAN.
- Communication fails between devices in different VLANs.

This confirms successful network segmentation.

## Lab File

The Packet Tracer lab file can be downloaded here:

[VLAN.pkt](vlan-network-lab.pkt)

## Screenshot

![Topology and Ping Test](topology_ping_test.png)

## Japanese Version

日本語版のREADMEはこちら：

[README_JP.md](./README_JP.md)
