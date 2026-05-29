# Azure Sentinel SOC Lab: RDP Brute-Force Detection and Attack Map Visualization

## Overview

This project documents a hands-on Microsoft Azure Sentinel SOC lab focused on monitoring failed RDP login attempts against an intentionally exposed Windows virtual machine.

The lab uses Microsoft Azure, a Windows virtual machine, Network Security Groups, Log Analytics Workspace, Azure Monitor Agent, Microsoft Sentinel, KQL, GeoIP enrichment, and Sentinel Workbooks to collect, investigate, and visualize authentication attack activity.

## Objective

The objective of this lab was to understand how endpoint security logs flow into a SIEM and how a SOC analyst can investigate failed authentication activity using KQL and visual dashboards.

## Lab Components

- Microsoft Azure subscription
- Azure Resource Group
- Azure Virtual Network and subnet
- Windows virtual machine
- Network Security Group with intentionally permissive inbound access for lab simulation
- Log Analytics Workspace
- Azure Monitor Agent
- Microsoft Sentinel
- KQL queries
- GeoIP enrichment
- Sentinel Workbook attack map

## Attack Scenario

A Windows VM was intentionally exposed to the public internet in a controlled lab environment. Failed RDP login attempts were collected from Windows Security logs and analyzed using Microsoft Sentinel and Log Analytics.

The main detection focus was Windows Security Event ID 4625, which represents failed logon attempts.

## Detection and Analysis

KQL was used to identify failed login attempts, summarize source IP addresses, review attempted usernames, and enrich IP addresses with GeoIP data for visualization.

The investigation focused on:

- Failed logon timestamps
- Attempted account names
- Source IP addresses
- Target computer name
- Repeated authentication failures
- GeoIP-based source location visualization

## Screenshots

The `screenshots/` folder includes redacted screenshots showing:

1. Sentinel Workbook attack map
2. Attack location summary
3. KQL query for failed logons
4. KQL results showing failed authentication activity
5. Azure resource visualizer
6. Network Security Group inbound rule
7. Risky inbound rule details used for the controlled lab exposure

## KQL Queries

The `kql/` folder includes reusable KQL queries for:

- Failed RDP logons
- Attacker IP summary
- Top targeted usernames
- GeoIP enrichment
- Workbook map visualization

## Key Learning Outcomes

This lab helped me practice:

- Azure VM deployment
- Cloud network exposure analysis
- Network Security Group rule review
- Windows Security Event Log collection
- Log Analytics Workspace usage
- Microsoft Sentinel onboarding
- KQL-based investigation
- GeoIP enrichment
- Workbook dashboard creation
- SOC-style documentation

## Security Note

This project was created for educational and portfolio purposes only. The VM exposure was intentional and temporary. Sensitive details such as credentials, subscription IDs, tenant IDs, full portal URLs, personal email addresses, and public target IP information were removed or redacted from screenshots and documentation.

## Author

Om Pingale
