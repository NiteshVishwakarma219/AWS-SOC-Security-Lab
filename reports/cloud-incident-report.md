# ☁️🚨 AWS Cloud Incident Response Report

## 🧾 Incident Title:
Suspicious Login Activity and Unauthorized AWS Resource Access Detected

---

## 📌 Incident Overview:
This report documents a simulated security incident in an AWS environment where suspicious login activity and unauthorized resource access were detected using AWS CloudTrail and Amazon GuardDuty.

---

## ⏱ Timeline of Events:

- 09:58 AM → User login detected from new IP address
- 10:00 AM → IAM user created with elevated permissions
- 10:03 AM → Multiple API calls detected (S3, IAM)
- 10:05 AM → GuardDuty generated HIGH severity alert
- 10:10 AM → Incident investigation started
- 10:15 AM → Access revoked and user disabled

---

## 🔍 Detection Tools Used:

### ☁️ AWS CloudTrail:
- Logged all API calls
- Tracked IAM user creation
- Recorded login events and source IPs

### 🛡 Amazon GuardDuty:
- Detected unusual login location
- Flagged suspicious API activity
- Generated security findings

### 📊 CloudWatch (Optional):
- Monitored security metrics
- Triggered alerts for abnormal behavior

---

## ⚠️ Indicators of Compromise (IOCs):

- Login from unfamiliar IP address
- IAM user created outside normal workflow
- Unusual S3 access attempts
- Multiple unauthorized API calls

---

## 🧠 Analysis:

The activity suggests a possible account compromise or unauthorized access attempt. The attacker attempted to escalate privileges by creating a new IAM user and accessing AWS resources such as S3.

---

## 🚨 Response Actions Taken:

- Suspicious IAM user disabled immediately
- Active sessions revoked
- Access keys rotated
- CloudTrail logs reviewed
- GuardDuty findings documented

---

## 🛡 Lessons Learned:

- Enable MFA for all IAM users
- Restrict IAM permissions using least privilege
- Continuously monitor CloudTrail logs
- Enable GuardDuty in all regions
- Set up real-time alerts via CloudWatch

---

## 📌 Conclusion:

The incident was successfully detected and mitigated using AWS-native security tools. This simulation demonstrates real-world SOC + Cloud Security incident handling capabilities.

---

## 👨‍💻 Author:
Nitesh Vishwakarma  
SOC + Cloud Security Enthusiast