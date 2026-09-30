# Azure Availability Set to Availability Zone Migration

## Project Overview
This project demonstrates the migration of a web workload from an Azure Availability Set-based environment to an Availability Zone-based architecture.

## Problem
Migration requires proper planning of VM placement, networking, Load Balancer configuration, health monitoring, and application availability.

## Proposed Solution
Deploy the workload across VMs in Availability Zone 1 and Zone 2, connect them through an Azure Load Balancer, and use health probes to maintain application availability during failures.

## Azure Resources
- Resource Group: rg-azure-ha-migration
- Availability Set: avset-demo
- Source VM: vm-as-1
- Zone 1 VM: vm-az-1
- Zone 2 VM: vm-az-2
- Load Balancer: lb-ha-demo
- Backend Pool: backend-ha
- Health Probe: probe-http
- Public IP: 138.91.32.79

## Implementation
1. Created the source Availability Set environment.
2. Assessed the existing web workload.
3. Prepared VMs in Availability Zone 1 and Zone 2.
4. Deployed the web workload on both target VMs.
5. Configured the Load Balancer and backend pool.
6. Configured an HTTP health probe.
7. Tested the application through the Load Balancer.
8. Simulated VM failure and verified continued application availability.

## Result
The target architecture demonstrates zone-based redundancy and application continuity during a VM failure.
