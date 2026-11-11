# AWS Resource Lister

A lightweight, robust Bash automation script designed to query the AWS API and instantly list active resources within a specified region. Built for DevOps engineers, cloud administrators, and FinOps teams looking to maintain visibility over cloud inventory and drive effective cost optimization.


## 💡The Problem: Cloud Waste and Visibility Gaps

As cloud environments scale, resources are frequently provisioned for development, testing, or temporary workloads and subsequently forgotten. Unmonitored EBS volumes, idle EC2 instances, forgotten S3 buckets, and running Lambda functions quietly accumulate, driving up monthly cloud spend.

This project solves this operational blind spot by providing a simple, dependency-light command-line utility that allows engineers to audit specific regions instantly without navigating the complex AWS Management Console. By making infrastructure inventory checks as easy as running a single shell command, teams can:

- **Accelerate Audits:** Quickly run targeted checks across regions to identify lingering workloads.
- **Support FinOps Initiatives:** Feed clean resource inventories into cost-optimization pipelines.
- **Enforce Accountability:** Standardize how teams inspect regional resource allocation before executing cleanup routines.


## 🛠️Prerequisites & Requirements

Before running the script, ensure your environment meets the following prerequisites:

- **Local Linux Machine or EC2 Instance:** A Unix-like shell environment (Bash).
- **AWS CLI Installed:** The AWS Command Line Interface must be installed to communicate with the AWS API.
- **AWS Credentials Configured:** Active AWS Access Key ID and Secret Access Key configured via aws configure or appropriate IAM role permissions.
- **Execution Permissions:** Appropriate permissions (chmod +x) to execute the script.

## 🚀Getting Started

### 1. Clone the Repository

Bash

```bash
  git clone https://github.com/Sheggel/AWS-Resource-Lister.git
cd aws-resource-lister
```


### 2. Configure AWS Credentials

Ensure your terminal session is authenticated with AWS:

Bash

```bash
  aws configure
```
*(Provide your AWS Access Key ID, Secret Access Key, default region, and output format when prompted).*


### 3. Grant Execution Permissions

Make the script executable:

Bash

```bash
 chmod +x aws_resource_list.sh
```

## 📖Usage

The script accepts two mandatory positional arguments: Region and AWS Service.

Bash

```bash
 ./aws_resource_list.sh <REGION> <SERVICE>
```

### Examples

**List active EC2 instances in** us-east-1:

Bash

```bash
 ./aws_resource_list.sh us-east-1 ec2
```

**List S3 buckets:** 

Bash

```bash
 ./aws_resource_list.sh us-east-1 s3
```

**List IAM users:** 

Bash

```bash
 ./aws_resource_list.sh us-east-1 iam
```




