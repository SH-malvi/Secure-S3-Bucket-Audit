## What was the problem?
I created an S3 Bucket on AWS and left it Public by mistake. Anyone could steal the data from it.

## What did I do?
1. Created an S3 Bucket and made it Public.
2. Accessed its data from another browser without login.
3. Then I secured it:
   - Turned ON Block All Public Access
   - Removed the Public Bucket Policy
   - Gave only Read permission to IAM User

## Result
The Bucket is now 100% Secure. The public link now shows "Access Denied".

## Tools Used
AWS S3, IAM, Bucket Policy
