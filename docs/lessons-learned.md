# Lessons Learned

This lab helped connect Azure infrastructure, Windows endpoint logging, and Microsoft Sentinel investigation workflows.

Key lessons:

- Internet-exposed cloud VMs can receive failed login attempts quickly.
- Network Security Groups control inbound cloud exposure and should be reviewed carefully.
- Windows Security Event ID 4625 is useful for failed login investigation.
- Log Analytics provides a central place to query collected logs.
- KQL is essential for filtering and summarizing security telemetry.
- GeoIP enrichment improves the readability of source IP activity.
- Sentinel Workbooks are useful for communicating attack patterns visually.
- Lab resources should be stopped or deleted after testing to reduce cost and risk.
