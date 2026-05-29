# Setup Notes

## Lab Steps

1. Created an Azure Resource Group.
2. Deployed a Windows virtual machine.
3. Configured virtual network and subnet resources.
4. Reviewed and modified Network Security Group rules for the lab scenario.
5. Connected the VM logs to a Log Analytics Workspace.
6. Enabled Azure Monitor Agent for log collection.
7. Connected Microsoft Sentinel to the workspace.
8. Queried Windows Security Event ID 4625 using KQL.
9. Added GeoIP enrichment for source IP analysis.
10. Created a Sentinel Workbook attack map.

## Cleanup

After completing the lab, the VM should be stopped or deleted. Any intentionally permissive inbound NSG rules should be removed. This helps avoid unnecessary cloud cost and reduces exposure risk.
