# SQL Filtering and Security Investigation Report

## Project Overview

As a cybersecurity analyst, my role is pivotal in safeguarding the organization’s data integrity and security. This project focuses on a detailed examination of our security logs to identify and investigate potential security incidents. By leveraging SQL queries, I filtered and analyzed data from critical tables such as `log_in_attempts` and `employees` to uncover suspicious activities that could signify security threats or breaches. The ultimate goal was to ensure that the organization’s systems remain secure and to preemptively address any vulnerabilities.

## Objectives and Queries

### 1. **Detect After Hours Failed Login Attempts**

**Objective:**  
To identify and analyze login attempts that occurred after standard business hours (18:00) and were unsuccessful. Monitoring after-hours login attempts is crucial as they may indicate unauthorized access attempts. Such activities, especially when they fail, could be a sign of malicious intent, and immediate investigation is required to prevent potential breaches.

**SQL Query:**

```sql
SELECT * 
FROM log_in_attempts 
WHERE login_time > '18:00' AND success = 0;
