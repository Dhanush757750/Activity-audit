
# EXPERIMENT 4
# NAME  : DHANUSH C
# REGNO : 212224040066

## ASSET-ORIENTED RISK ASSESSMENT OF STORAGE ASSETS IN AWS 

---

## Aim

To identify storage assets in **AWS S3**, identify possible vulnerabilities and threats, and assess their likelihood, impact, and risk level.

---

## Software / Cloud Services Required

- AWS Account
- Microsoft Azure Account
- Web Browser
- Internet Connection

### Cloud Services Used

| Cloud Platform | Storage Service |
|---|---|
| AWS | Amazon S3 |

---

# PART A — AWS S3 STORAGE ASSESSMENT

## Step 1: Login to AWS

1. Open the AWS Management Console.
2. Sign in using your AWS account.
3. Search for **S3**.
4. Select **Amazon S3**.

---

## Step 2: Select the S3 Bucket

1. Click **Buckets**.
2. Select the S3 bucket created in the previous experiment.
3. Record:
   - Bucket name
   - AWS Region
   - Number/type of objects

<img width="1536" height="960" alt="Screenshot 2026-08-25 103950" src="https://github.com/user-attachments/assets/3d9d0280-264b-435a-b639-9b2204494c31" />

---

## Step 3: Check Block Public Access

1. Open the S3 bucket.
2. Select **Permissions**.
3. Locate **Block public access (bucket settings)**.
4. Check **Block all public access**.

### Record

- **ON** → Secure configuration
- **OFF** → Potential public-access risk

<img width="1535" height="960" alt="Screenshot 2026-08-25 104020" src="https://github.com/user-attachments/assets/f9c101ca-dcb7-4792-82e8-5db31c62ad7f" />

---

## Step 4: Check Bucket Versioning

1. Select the **Properties** tab.
2. Locate **Bucket Versioning**.
3. Record whether it is:
   - Enabled
   - Disabled

### Security Purpose

Versioning helps recover previous versions of objects after accidental deletion or modification.

<img width="1536" height="960" alt="Screenshot 2026-08-25 104633" src="https://github.com/user-attachments/assets/0654c1ff-f5db-4683-be2e-d67e67f94929" />

---

## Step 5: Check Default Encryption

1. Stay in the **Properties** tab.
2. Locate **Default encryption**.
3. Record the encryption type.

### Possible Configurations

- SSE-S3
- SSE-KMS
- DSSE-KMS

### Security Purpose

Encryption protects stored data from unauthorized disclosure.

<img width="1536" height="960" alt="Screenshot 2026-08-25 104731" src="https://github.com/user-attachments/assets/18eeb0a4-b810-4d13-9e0b-ade6de998471" />

---

## Step 6: Check Bucket Policy

1. Select **Permissions**.
2. Locate **Bucket policy**.
3. Check whether a bucket policy exists.

### Record

- Policy exists
- No policy

> **Note:** A missing bucket policy is not automatically a vulnerability. Access may be controlled through IAM and other AWS security mechanisms.

<img width="1524" height="958" alt="Screenshot 2026-08-25 104832" src="https://github.com/user-attachments/assets/5d8f0ce2-2679-4924-a8d8-5832fc29bf7b" />

---

## Step 7: Check Object Ownership and ACL

1. In **Permissions**, locate **Object Ownership**.
2. Record the current configuration.

A common secure configuration is:

**Bucket owner enforced**

This means:

- ACLs are disabled.
- Objects are owned by the bucket owner.
- Access is controlled using policies.

<img width="1535" height="960" alt="Screenshot 2026-08-25 104914" src="https://github.com/user-attachments/assets/5a979c97-ea99-46b0-8273-a9617964783a" />

---
## Step 8: Check Server Access Logging

1. Go to **Properties**.
2. Locate **Server access logging**.
3. Record whether it is:
   - Enabled
   - Disabled

### Security Purpose

Logging helps investigate suspicious or unauthorized access to the bucket.

<img width="1536" height="960" alt="Screenshot 2026-08-25 105006" src="https://github.com/user-attachments/assets/aa7022b5-08da-4f3c-b92e-e965a1ee1d2d" />

---


## Step 7: Check Object Ownership and ACL

1. In **Permissions**, locate **Object Ownership**.
2. Record the current configuration.

A common secure configuration is:

**Bucket owner enforced**

This means:

- ACLs are disabled.
- Objects are owned by the bucket owner.
- Access is controlled using policies.

<img width="1536" height="960" alt="Screenshot 2026-08-25 105042" src="https://github.com/user-attachments/assets/f0286acb-931f-42a1-9fc9-dae10141f4cb" />

---


---

# PART B — AWS RISK ASSESSMENT

After checking the S3 configuration, identify possible vulnerabilities and threats.

## Risk Formula

**Risk Score = Likelihood × Impact**

### Likelihood Scale

| Score | Description |
|---:|---|
| 1 | Very Low |
| 2 | Low |
| 3 | Medium |
| 4 | High |
| 5 | Very High |

## AWS Risk Assessment

> Students must use their actual configuration while preparing the final table.

| Asset | Vulnerability | Threat | Likelihood | Impact | Risk Score | Risk Level | Recommended Mitigation |
|---|---|---|---:|---:|---:|---|---|
| S3 Bucket | Versioning disabled | Accidental/malicious data deletion | 3 | 4 | 12 | High | Enable versioning |
| S3 Bucket | Access logging disabled | Difficult investigation of unauthorized activity | 3 | 3 | 9 | Medium | Enable appropriate logging |
| S3 Bucket | Public access enabled | Unauthorized data access | 4 | 5 | 20 | Critical | Enable Block Public Access |
| S3 Bucket | Weak access permissions | Unauthorized modification/access | 3 | 4 | 12 | High | Apply least privilege |

---

Risk scores were calculated using the **Likelihood × Impact** method, and appropriate security mitigation measures were recommended.


## Result

~~~
AWS S3 security configurations were analyzed and potential risks were identified.
Risk levels were assessed and suitable security measures were recommended. 
~~~



