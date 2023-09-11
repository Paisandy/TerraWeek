# 7 Days Terraweek Challenge: Day 1 - Getting Started with Terraform
Greetings Terraform enthusiastic, I have accepted Terraweek Challenge, So let's begin
## Day1: Introduction to Terraform and Terraform Basics

Before diving into Terraform, it's essential to grasp the concept of **Infrastructure as Code (IaC)**. So, let's rephrase your sentences and provide a brief explanation:
"Let's begin by understanding Infrastructure as Code (IaC) before delving into Terraform."

Explanation:
**Infrastructure as Code (IaC)** is a methodology that involves managing and provisioning infrastructure resources, such as servers, networks, and databases, using code and automation tools. It allows you to define your infrastructure configurations as code, enabling easier management, version control, and reproducibility of your infrastructure environments. Terraform is one of the popular tools used for implementing IaC, helping you create, modify, and manage infrastructure resources through code-based configurations.

There are Various IaC tools like Terraform, Chef, Puppet and Ansible.
**"Read this blog to understand why Terraform is the preferred choice and the best option for infrastructure provisioning."**

## What Is Terraform?
Terraform is a tool for provisioning, managing, and deploying infrastructure resources. It is an open-source tool written in Golang and created by the HashiCorp company. With Terraform, you can manage infrastructure for your applications across multiple cloud providers - AWS, Azure, GCP, etc. - using a single tool.
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/9a8228b4-49f5-4e8b-b668-bc844b17c8e8)
To get started with Terraform, developers simply need to download the Terraform binary, choose which (https://developer.hashicorp.com/terraform/language/providers) they'll be working with, create some (https://developer.hashicorp.com/terraform/language/providers/configuration)

## How Infrastructure as Code works?
Without IaC, the team would individually configure the infrastructure (servers, databases, load balancers, containers, etc.) for each deployment. Over time, environments that were intended to be identical, become inconsistent (they are often called “snowflakes”), which makes them harder to configure and subsequently slows down deployments.
So, IaC uses software tools to automate administrative tasks by describing infrastructure in code.

It’s implemented like this:

The team writes infrastructure configurations in a required programming language.
The code files are sent to a code repository.
An IaC tool runs the code and performs the required activities.
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/9616fc1a-8487-41ab-a6d9-c59961457d61)

## How can it help you manage Infrastructure as Code?
Terraform is a tool that assists in managing infrastructure as code. It enables you to define and provision infrastructure resources through code, simplifying the management and automation of your infrastructure.

## Why do we need Terraform and how does it simplify infrastructure provisioning?
Terraform works as an Infrastructure as Code (IaC) tool by allowing users to define infrastructure as code using the HashiCorp Configuration Language (HCL). Following are the steps involved in working with Terraform as an IaC tool:

Configuration:
Define the desired infrastructure in Terraform configuration files using the HashiCorp Configuration Language (HCL).
Initialization:
Initialize the working directory and download the necessary provider plugins and modules.
Planning:
Create an execution plan that shows what Terraform will do when you apply the configuration. This step analyzes the current infrastructure state and determines which resources must be created, updated, or destroyed to reach the desired state.
Applying:
Apply the changes to the infrastructure by creating, updating, or destroying resources as per the execution plan.
Provisioning:
Terraform can automatically provision the software and configurations on the infrastructure once the resources are created.
Change Management:
Any changes to the infrastructure can be managed using the same configuration files and applied in the same way, providing a consistent and repeatable process.
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/aab278ba-948b-477b-8ad9-a14f4cf7652f)

## How can you install Terraform?
The Best Practice for the Terraform using Visual Studion on to a Local Machine
**Steps to Follow**
1. Install Visual Studio Code (https://code.visualstudio.com/download)
2. Install AWS CLI (https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) On Windows **Download and run the AWS CLI MSI installer for Windows (64-bit)**
3. Install Terraform (https://developer.hashicorp.com/terraform/downloads) for Window **AMD64**
4. Install Git Bash (https://developer.hashicorp.com/terraform/downloads)

After Installing. Let's setup it.
**Click on Windows Button --> Search "Edit The Environment Variables" --> Click on the "Environment Variables"**
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/7e9b0013-8416-436d-bafc-f8aa8c9cc0f9)
**Click on the Path --> Click on the new --> Copy the Path which You Installed Terraform --> Click Ok**
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/c44dc94b-7df2-4b54-91e4-404207f25fb9)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/7135773a-3804-4d28-ad09-1a577dbf6f4a)
**Click ok**
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/d24d427c-41e3-46da-bc15-750bfbdc691a)

Same Follow the steps AWS CLI, Git Bash.

Open Visual Studio Code 
5. Run the below code. It is Installed or not
```
terraform --version
```
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/6c6faf81-ee9e-4091-aec7-46b3a916e679)
```
aws --version
```
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/9f79c352-e76b-4b21-a5f4-f30d912bec4d)

## Blocks and Arguments
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/eb79814d-e4e0-453e-a947-65220a278dd6)
1. A block is a container for other content and An argument assigns a value to a particular name:
2. filename = pai.txt"
3. The identifier before the equals sign is the argument name, and the expression after the equals sign is the argument's value.
4. Resource block: block name used to mention the type of the block. The resource block expects two labels, which are local_file and “pai” in the example above. A particular block type may have any number of required labels, or it may require none.
5. Local = provider, file = type, “pai” name of the resource.
6. Then we have arguments, filename, content, etc
7. We can have multiple resources

## Execution of Infrastructure
**terraform init --> terraform plan --> terraform apply**
### Terraform Init
```
terraform init
```
This command will scan your tf files in that folder and install all the required
automation things.
### Terraform Plan
```
terraform plan
```
This command will create an execution plan for terraforming, the things that will be installed, the names, and the properties added.
### Terraform Apply
```
terraform apply
```
The actual execution and automation happen in this command.

## Connect to AWS Cloud
You must have an AWS Account to proceed with the below steps:
### 1. Create IAM User
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/757f11e9-30c0-4d28-b1dd-0ac4aa41649c)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/8504cf99-bc49-4d71-92b0-4028aef3daf3)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/1dbc8e46-abf4-482b-8a68-0832c6d2b8f1)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/3a9279fe-9d7f-4a4b-988b-71062e2cefbe)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/afce6c62-3861-4123-a881-b439c92a2788)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/320d1ec3-155b-4541-814c-9215e3010b4a)

**Scroll Down Click on NEXT**
**Click on Add New Tag**
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/ed9b7ad9-b65b-4fb7-9631-7cf502730f43)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/6637b0c6-bbc8-4817-8984-b97619aa1977)
Download .csv file and Click on Return to users 
Finally! User is Created.

### 2. Login to aws cli
**First you need to create a Security Credential. to login aws cli**
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/6007e9d8-611d-4f5c-8021-200496b9f88d)
Click on the Security Credential
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/78a8f0ac-177a-4d5e-9698-d1661d3b72d3)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/e0e85a58-a495-48bf-94a6-995aed87e255)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/a69595a7-d772-4227-97af-913241531112)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/bf547b41-2c24-4c9f-a255-8f5acfbd0530)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/a7666c4c-b154-4290-b462-8c6d690e5e29)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/3e8d9302-877e-41be-bbdc-f65a32b57398)

**Go to the Visual Studio Terminal**
Copy this command
```
aws configure
```
**Give your AWS Access Key ID, AWS Secret Acess Key, Default Region Name, Default output format**
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/4f87169a-ad2c-45f4-bef4-eac5dbff4b3b)

Create a Folder and Start aws terraform coding

### Terraform Plugin for AWS CLI
copy the code
```
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}
```
Terraform Plugins that allow it to coomunicate with various infrastructure and service providers. Terraform can handle the resource and data source specific to each. For example - you can use aws provider of aws to allow terraform to manage aws resources.

### Let's start automate using terraform to creating a Ec2 Instance and S3 Bucket
here is code
```
# Creating S3 Bucket
provider "aws" {
  region = "us-east-1"
}

resource "aws_s3_bucket" "demo-bucket" {
  bucket = "my-bucket-oii"

  tags = {
    Name        = "My bucket"
    Environment = "Dev"
  }
}

# Creating Ec2 Instance
resource "aws_instance" "my-instance" {
  ami           = "ami-053b0d53c279acc90"
  instance_type = "t2.micro"
  tags = {
    "Name" = "MyInstanceEc2"
  }
}
```
**Should Provide a Region base on your choice**
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/260c6e88-0916-4551-b226-f412e05994cc)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/71552da0-1d9b-424f-893c-d49b8a959028)

After writing the code
apply this command
```
terraform init
```
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/3179fe9b-8599-43ad-849f-d7a0cb778dce)

next apply command **terraform fmt**
The terraform fmt command is used to rewrite Terraform configuration files to a canonical format and style.
```
terraform fmt
```

next apply command **terraform validate**
The terraform validate command is used to validate the syntax of Terraform files. Terraform performs a syntax check on all Terraform files in the directory specified and displays warnings and errors if any files contain invalid syntax.
```
terraform validate
```
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/7c69806b-35be-4263-ad91-77f1c5fd8a64)

next apply coomand **terraform plan**
```
terraform plan
```

nexy apply command **terraform apply**
```
terraform apply
```
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/df57801c-b4d8-4a19-9837-af361b8183dd)
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/1fd15b80-ff6a-46d9-ba3c-74b75bff3a4e)

### Finally done!! Let's see 
**S3 Bucket**
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/5b115340-7751-4506-b431-c7b96236e054)
**Ec2 Instance**
![image](https://github.com/Paisandy/TerraWeek/assets/115485972/1ba48a9f-d125-4443-8711-ec40898b69e3)

## Conclusion
You did it! You learned how to use Terraform, See the magic how automation work. Practice it more. Do hands on experience. Will see next blog.
