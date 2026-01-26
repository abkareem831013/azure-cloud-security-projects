# Project 4 – Azure Activity Logs Monitoring

## Overview
This project demonstrates how to configure **Azure Activity Log diagnostic settings** to collect subscription-level logs and analyze them using **Azure Log Analytics and KQL** for security monitoring.

## Objectives
- Enable Azure Activity Logs at subscription level
- Send logs to Log Analytics workspace
- Query administrative and security events using KQL
- Gain visibility into Azure control-plane activities

## Azure Services Used
- Azure Subscription
- Azure Activity Log
- Diagnostic Settings
- Log Analytics Workspace
- KQL (Kusto Query Language)

## Architecture
Azure Subscription  
→ Activity Logs  
→ Diagnostic Settings  
→ Log Analytics Workspace  
→ KQL Queries

## Implementation Steps

### Step 1: Create Log Analytics Workspace
- Created a Log Analytics workspace (`law-security-demo`)
- Used it as a centralized log collection point

### Step 2: Configure Activity Log Diagnostic Settings
- Navigated to **Subscription → Activity Log**
- Enabled **Diagnostic settings**
- Selected log categories:
  - Administrative
  - Security
  - Policy
- Sent logs to Log Analytics workspace

### Step 3: Generate Azure Activity
- Generated new management events by:
  - Adding resource tags
  - Accessing Azure services
- Ensured logs were created after diagnostics were enabled

### Step 4: Query Logs Using KQL
```kql
AzureActivity
| sort by TimeGenerated desc
| take 10
