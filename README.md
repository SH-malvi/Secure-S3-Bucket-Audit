# Secure S3 Bucket Audit - AWS Cloud Security Project

## Objective
To identify and fix public access misconfiguration in an AWS S3 bucket.

## Vulnerability Found (Before Fix)
I created a test bucket and found 2 critical issues:
1.  Block All Public Access was OFF
2.  Bucket Policy had `"Principal": "*"` which means open to everyone

This is a major security risk - anyone on the internet can read data.

## Remediation Steps (How I Fixed It)
1.  Enabled **Block All Public Access** from S3 Permissions tab
2.  Deleted the public Bucket Policy with Principal *
3.  Created a new policy with Least Privilege - only my IAM user can access
4.  Enabled Server-Side Encryption (SSE-S3)

## After Fix
- Bucket is now private
- Only authorized user can access
- Public access blocked

## Tools Used
AWS S3, IAM, Bucket Policy, Block Public Access

## What I Learned
- How to check S3 misconfigurations
- Importance of Least Privilege
- How to secure a public bucket

---
**Author:** Shraddha Malvi | Aspiring Cloud Security / SOC Analyst

