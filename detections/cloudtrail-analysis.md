# ☁️ CloudTrail Analysis – SOC Investigation Report

## 🎯 Objective
Analyze AWS CloudTrail logs to identify suspicious or unauthorized activity in the AWS environment.

---

## 🔍 Data Source
- AWS CloudTrail Logs
- S3 stored audit logs
- IAM activity logs
- API call history

---

## 🚨 Key Events Analyzed

### 🔴 1. New IAM User Creation
- Event: CreateUser
- Source: IAM Console/API
- Risk: Unauthorized privilege escalation attempt

**Observation:**
A new IAM user was created without proper justification or approval workflow.

---

### 🔴 2. Console Login from New IP
- Event: ConsoleLogin
- Source IP: Unknown / New geographic location
- Risk: Credential compromise or brute force success

**Observation:**
Login detected from unfamiliar IP address.

---

### 🔴 3. S3 Bucket Access Attempt
- Event: GetObject / ListBucket
- Target: Sensitive S3 bucket
- Risk: Data exfiltration attempt

**Observation:**
Multiple unauthorized access attempts detected on S3 resources.

---

## 🧠 SOC Analysis

Based on logs:
- Activity indicates possible compromised credentials
- IAM privilege escalation attempt detected
- Suspicious API usage pattern observed

---

## 🚨 Response Actions
- Disabled suspicious IAM user
- Revoked active sessions
- Restricted S3 bucket access
- Enabled MFA enforcement

---

## 📌 Conclusion
CloudTrail logs successfully helped identify and trace unauthorized AWS activity. This demonstrates strong cloud security monitoring and SOC investigation capability.
