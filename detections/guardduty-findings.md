# 🛡️ AWS GuardDuty Findings – Threat Detection Report

## 🎯 Objective
Analyze GuardDuty alerts to detect malicious or suspicious behavior in AWS environment.

---

## 🔍 Data Source
- AWS GuardDuty Findings
- CloudTrail correlation logs
- VPC flow logs (if enabled)

---

## 🚨 Key Findings

---

### 🔴 1. Unauthorized Access (Recon Activity)

- Finding Type: Recon:EC2/PortProbeUnprotectedPort
- Severity: Medium
- Resource: EC2 instance

**Observation:**
Port scanning activity detected targeting EC2 instance.

---

### 🔴 2. Suspicious Login Attempt

- Finding Type: UnauthorizedAccess:IAMUser/ConsoleLogin
- Severity: High
- Source IP: Unknown location

**Observation:**
Login attempt from unusual geographic location.

---

### 🔴 3. API Abuse Detection

- Finding Type: Policy:IAMUser/RootCredentialUsage
- Severity: Critical

**Observation:**
Root-level credential usage detected which violates security best practices.

---

## 🧠 SOC Analysis

GuardDuty indicates:
- Possible credential compromise
- Unauthorized reconnaissance activity
- Policy violation (root access usage)

---

## 🚨 Response Actions

- Disabled affected IAM credentials
- Enabled MFA for all users
- Blocked suspicious IPs
- Initiated incident response workflow

---

## 📌 Conclusion

GuardDuty effectively detected early-stage attack behavior and provided actionable security insights, demonstrating strong cloud threat detection capabilities.