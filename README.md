# Isolated Traffic-Flood Lab

Course lab from Introduction to Networks, completed in Fall 2025.

## Purpose

I built this lab to observe how a small test service behaved when it received more traffic than it could handle. The test stayed inside an isolated VirtualBox network and did not target any public system.

## Lab setup

- Two Ubuntu virtual machines in VirtualBox
- One machine running the test service
- One machine generating controlled lab traffic
- Wireshark for packet capture and review
- Linux `top` for system load and recovery checks

## What I observed

- Wireshark showed the repeated traffic pattern between the two lab machines
- Linux `top` showed increased system load while the test was running
- The host recovered after the controlled traffic stopped

The exercise made the availability side of security easier to understand. Packet captures showed the traffic pattern, while the system measurements showed what that traffic meant for the host.

## Mitigations I reviewed

- Rate limiting
- Traffic monitoring and alerting
- Basic filtering and access control lists
- Firewalls and layered network controls
- Load balancing and content delivery networks for larger services

## Repository scope

This repository is a short lab record. I did not publish the traffic-generation script or packet captures because they are not needed to explain the work and could expose unnecessary environment details.
