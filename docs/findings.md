# Findings

## Summary

The lab observed failed authentication activity against an intentionally exposed Azure Windows VM. The activity was investigated through Windows Security Event ID 4625.

## Observed Patterns

The investigation showed:

- Failed logon attempts against the exposed VM
- Multiple attempted account names
- Public source IP addresses attempting authentication
- Repeated failed authentication behavior
- Geographic distribution of source IPs through GeoIP enrichment

## SOC Relevance

This is relevant to SOC work because exposed RDP services are common targets for brute-force activity. Monitoring Windows Security Event ID 4625 helps analysts detect failed login patterns, repeated authentication attempts, and potentially malicious source IP activity.

## Analyst Takeaway

Raw event logs are useful, but they become much more effective when combined with:

- KQL filtering
- Source IP summarization
- Account targeting review
- GeoIP enrichment
- Workbook-based visualization
