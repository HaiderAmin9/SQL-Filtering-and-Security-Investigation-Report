# SQL Filtering and Security Investigation Report

## Project Overview

As a cybersecurity analyst, this project involves a thorough examination of the organization's security data to identify and investigate potential security incidents. Utilizing SQL queries, I filtered and analyzed data from the `log_in_attempts` and `employees` tables to address specific security concerns and ensure the organization's data integrity. The goal was to pinpoint suspicious activities and anomalies that could signify security threats or breaches.

## Objectives and Queries

### 1. **Detect After Hours Failed Login Attempts**

**Objective:** 
To identify login attempts that occurred after standard business hours (18:00) and were unsuccessful. This analysis is crucial for detecting unauthorized access attempts that happen outside of regular operational hours, which may indicate potential malicious activities or security breaches. Such after-hours activities are often more suspicious as they fall outside normal usage patterns, increasing the risk of security incidents.

**SQL Query:**

```sql
SELECT * 
FROM log_in_attempts 
WHERE login_time > '18:00' AND success = 0;
