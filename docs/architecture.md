# Architecture

## High-Level Flow

The lab architecture used an Azure-hosted Windows virtual machine as the endpoint generating Windows Security Event Logs. These logs were collected through Azure Monitor Agent and sent to a Log Analytics Workspace.

Microsoft Sentinel was connected to the Log Analytics Workspace for SIEM-style monitoring and investigation. KQL queries were used to analyze failed logon attempts. GeoIP data was used to enrich attacker source IP addresses and display them on a Sentinel Workbook map.

## Components

- Windows VM: Internet-exposed test endpoint used for the lab
- Network Security Group: Controlled inbound exposure for the simulation
- Log Analytics Workspace: Central log storage and query layer
- Azure Monitor Agent: Log collection agent
- Microsoft Sentinel: SIEM layer
- KQL Queries: Investigation and detection logic
- GeoIP Watchlist: IP-to-location enrichment
- Sentinel Workbook: Visualization layer

## Data Flow

1. Failed login attempts were generated against the exposed Windows VM.
2. Windows Security Event Logs captured failed authentication events.
3. Azure Monitor Agent forwarded relevant logs to Log Analytics.
4. Microsoft Sentinel used the workspace as its data source.
5. KQL queries filtered and summarized failed logon activity.
6. GeoIP enrichment mapped source IPs to approximate locations.
7. Sentinel Workbook visualized the attack sources.
