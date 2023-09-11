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


