# Project 5 – Azure SIEM using Microsoft Sentinel

## Overview
This project demonstrates the implementation of a cloud-native SIEM solution using Microsoft Sentinel to monitor, detect, and investigate security events in an Azure environment.

## Objectives
- Enable Microsoft Sentinel on Log Analytics workspace
- Connect Azure Activity Logs to Sentinel
- Analyze logs using KQL
- Gain hands-on experience with SIEM concepts

## Services Used
- Microsoft Sentinel
- Azure Activity Logs
- Log Analytics Workspace
- Azure Monitor
- KQL (Kusto Query Language)

## Architecture
Azure Subscription  
→ Azure Activity Logs  
→ Log Analytics Workspace  
→ Microsoft Sentinel (SIEM)  
→ Security Analysis using KQL

## Implementation Steps

### Step 1: Enable Microsoft Sentinel
- Enabled Sentinel on existing Log Analytics workspace (law-security-demo)

### Step 2: Connect Azure Activity Logs
- Installed Azure Activity solution from Microsoft Sentinel Content Hub
- Verified Azure Activity data connector status as Connected

### Step 3: Log Analysis using KQL
```kql
AzureActivity
| take 10

