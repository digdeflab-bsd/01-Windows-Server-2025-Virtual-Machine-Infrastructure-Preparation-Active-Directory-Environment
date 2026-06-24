# Lab Project: Virtual Machine Infrastructure Preparation for an Active Directory Environment

![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)

https://youtu.be/KnhSBXCeN7Y

## Project Summary
![Windows Server](https://img.shields.io/badge/Windows_Server-0078D6?style=for-the-badge&logo=windows&logoColor=white)

This lab project focused on preparing the virtual infrastructure required for a Windows Server 2025 Active Directory environment. The work involved designing and configuring virtual machines before operating system installation, including a Windows Server 2025 virtual machine that would later be promoted to a Domain Controller and two Windows 11 Enterprise LTSC workstations that would later be joined to the domain.

## Goal

To build a controlled virtual lab environment that supports future Active Directory deployment, domain services configuration, and Windows workstation integration.

## Lab Environment

### Host System

* Windows 11 host machine
* Intel Core i5 processor
* 40 GB RAM
* 500 GB NVMe storage
* 1 TB SSD storage

### Virtualization Platform

* VMware Workstation Pro 25H2U1

### Network Infrastructure

* pfSense virtual firewall/router
* Default gateway: 192.168.60.1
* Network subnet: 192.168.60.0/24

The pfSense virtual machine was used as the central router and gateway for all lab systems, providing network connectivity within the virtual environment.

## Virtual Machine Configuration

### Windows Server 2025

Planned role:

* Future Active Directory Domain Controller

Initial configuration:

* 2 vCPUs
* 4 GB RAM
* 60 GB SSD storage
* Custom network adapter connected to pfSense VMnet1
* Static IP address: 192.168.60.80

Adjustment made:

* Increased memory allocation from 4 GB to 8 GB after observing performance slowdowns during lab setup.

### Windows 11 Enterprise LTSC Workstations (2)

Planned role:

* Domain-joined client workstations

Configuration for each workstation:

* 2 vCPUs
* 4 GB RAM
* 64 GB storage
* Custom network adapter connected to pfSense network
* IP addressing provided through DHCP

## Technical Decisions

### Dedicated Virtual Network

A custom virtual network connected through pfSense was used to isolate and manage communication between the lab systems.

### Static Addressing for the Server

The Windows Server virtual machine was assigned a static IP address to provide consistent network identification for future domain services.

### DHCP for Client Systems

The Windows 11 workstations were configured to receive IP addresses automatically, reflecting a common enterprise workstation deployment approach.

### Resource Adjustment

After observing performance limitations, the server's memory allocation was increased from 4 GB to 8 GB to improve virtual machine responsiveness.

## Skills Demonstrated

* Virtual lab design and planning
* VMware Workstation Pro administration
* Virtual machine provisioning
* Resource allocation and performance tuning
* Network configuration and segmentation
* pfSense virtual networking
* Static and DHCP IP addressing
* Windows Server infrastructure preparation
* Active Directory environment planning
* Documentation of lab configurations

## Outcome

Successfully prepared the virtual infrastructure required for a future Active Directory deployment by creating and configuring a Windows Server 2025 virtual machine and two Windows 11 Enterprise LTSC workstations within an isolated pfSense-managed network environment.

