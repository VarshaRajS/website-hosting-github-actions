![Screenshot_20240908-215530~2(2)](https://github.com/user-attachments/assets/ad3e604f-cfc8-4cd9-ad5d-11b0a00b1187)

**Project Overview:** Hosting a Website on Amazon S3 Using GitHub Actions

In this project, I successfully hosted a website on an Amazon S3 bucket, leveraging GitHub Actions for automated deployment. The workflow involved integrating GitHub Actions to create a CI/CD pipeline that streamlined the process of deploying website updates directly from the repository to the S3 bucket.
Key Features:

**1. Continuous Integration and Deployment:** Utilized GitHub Actions to automate the build and deployment process. Each push or pull request to the repository triggered the workflow, ensuring that any changes were tested and deployed seamlessly to the S3 bucket.

**2. Static Website Hosting on Amazon S3:** Configured an Amazon S3 bucket to host a static website, taking advantage of S3's scalability, durability, and high availability to serve web content efficiently.

**3. Security and Access Management:** Implemented AWS Identity and Access Management (IAM) roles and policies to securely manage access to the S3 bucket, ensuring only authorized actions were permitted.

**4. Version Control and Rollbacks:** Leveraged GitHub's version control capabilities, allowing easy rollbacks to previous website versions if necessary.

**Outcome:**

This setup ensures a robust, scalable, and cost-effective solution for hosting a static website, with an automated and reliable deployment pipeline that reduces manual intervention and minimizes downtime.

**Usage:**

1. Create an s3 bucket, under properties tab enable static website hosting
2. Under permissions tab, set suitable bucket policy:
   {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::web-hostings/*"
        }
    ] 
   }
3. Create IAM user and provide required access, create security credentials
4. Add the AWS_ACCESS_KEY and AWS_SECRET_ACCESS_KEY in the 
