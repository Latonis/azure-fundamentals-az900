# AZ-900 Microsoft Azure Fundamentals

Let this page be my study notes for AZ-900 course notes.

## **Introduction**

Course will cover:

- Exams are more relevant to the roles and their requirements

### Portal Features:

- Personalize
- Access Control
- Cost Management
- One Stop Shop
- Constantly Updated
- Multi-Platform

### Azure Command Line Interface:

Coffee to VM analogy (Many ways to make the cup of coffee - Portal, CLI, etc.)

Advantages:

- Stable
- Structured very logically
- Cross Platform
- Automation for future use
- Keep track of what with logging and version control

### PowerShell:

- Comes pre-installed, text only
- Cmdlet
    - New-AzVm
- Azure Resource Manager
- Versatile

### Cloud Shell:

Interactive browser-accessible shell for managing Azure resources

Stand-Alone or In-Portal

Features:

Access

Shell

Tools

Storage

Integrated File Editor

### Azure Mobile Apps:

On Android and iOS

Do Azure things in the app

Shows quick information on the go

Health

Resources

Alerts

Uses Azure Resource Manager

Use Cloud Shell from phone

### ARM Templates:

[https://azure.microsoft.com/resources/templates/?WT.mc_id=ACloudGuru_Learn_multiple-learn-wwl](https://azure.microsoft.com/resources/templates/?WT.mc_id=ACloudGuru_Learn_multiple-learn-wwl)

Describe resource usage

Common Syntax

Idempotent

Run templates as many times as you like, outcome is the same

Written in JSON

Source Control

Keep track of all changes

Reuse

Use combination of multiple partial ARM templates to achieve success

Declarative

Specify what needs to be done, not exactly how it should be done

No Human Errors

- [x]  Create Free Azure Account

### Summary of Chapter 1:

Course Overview

Benefits

Structure of Course

Azure Portal

One-stop shop for managing all Azure resources

Azure CLI

text-only way of managing Azure resources

Azure PowerShell

uses cmdlets to manage Azure resources

Azure Cloud Shell

Works from anywhere a browser does

Azure Mobile Apps

Manage Azure on the Go

Arm Templates

Automate Azure infrastructure setup via ARM templates

### First two labs

```json
SSH key files '/home/cloud/.ssh/id_rsa' and '/home/cloud/.ssh/id_rsa.pub' have been generated under ~/.ssh to allow SSH access to the VM. If using machines without permanent storage, back up your keys to a safe location.
{
  "fqdns": "",
  "id": "/subscriptions/4cedc5dd-e3ad-468d-bf66-32e31bdb9148/resourceGroups/72-cb9e7b76-accessing-and-using-the-azure-cloud-sh/providers/Microsoft.Compute/virtualMachines/newVM",
  "location": "westus",
  "macAddress": "00-22-48-09-7D-32",
  "powerState": "VM running",
  "privateIpAddress": "10.0.0.4",
  "publicIpAddress": "40.78.108.17",
  "resourceGroup": "72-cb9e7b76-accessing-and-using-the-azure-cloud-sh",
  "zones": ""
}
```

```powershell
Remove-AzVM -name newVM -ResourceGroupName 72-cb9e7b76-accessing-and-using-the-azure-cloud-sh

Virtual machine removal operation
This cmdlet will remove the specified virtual machine. Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

OperationId : 93348fdc-73ec-4959-9165-347e46337047
Status      : Succeeded
StartTime   : 1/5/2021 9:06:02 PM
EndTime     : 1/5/2021 9:06:44 PM
Error       :
```

AZ-900 Microsoft Azure Fundamentals 2020 - Introduction Quiz: 100%

## Cloud Concepts

[What is cloud computing? - Learn](https://docs.microsoft.com/en-us/learn/modules/principles-cloud-computing/2-what-is-cloud-computing?WT.mc_id=ACloudGuru_Learn_multiple-learn-wwl)

### The Language of Cloud Computing

**High Availability**

Core to the cloud

Traditional:

Owning the hardware

Physical access

cant just add servers

Cloud:

Don't down the hardware

add more severs with a click

if hardware fails, replace instantly

Use clusters to ensure high availability

**Fault Tolerance**

Resilience

Fault tolerance is part of the resilience of cloud computing

Zero Down-Time

Faults caused by Azure are also mitigated by Azure

**Disaster Recovery**

Catastrophic Disaster

Hurricane, flood, tornado, or cyber attacks are real threats

Plan to Recover

Complete plan to recover critical business systems

Specific Points

Designated Time to Recovery and Recovery Point

**Scalability**

Add more resources on an as-needed basis

Scaling out:

Add more resources to the application to mitigate

Scaling up:

Adding more computer power or resources to the current hardware

Scaling down:

Taking away computer power or resources from the current hardware

Auto-scaling occurs by rules set by the system-admins for when to scale up or back down

time

traffic

load

etc.

**Elasticity**

Ability to quickly expand or decrease computing resources, not just VMs.

Elasticity enables scaling

**Agility**

The ability to rapidly develop, test, and launch software applications that drive business growth

Review:

**High availability** means VMs can spin up fast to help process requests

**Fault tolerance** describes how Azure will ensure you have zero downtime for services provided by Azure

**Disaster recovery** uses time to recovery and recovery point metrics to recover from catastrophic failures

**Scalability** refers to scaling out or scaling up

**Elasticity** is the ability to quickly increase or decrease computer processing and resources

**Agility** means the ability to rapidly develop, test, and launch software applications

[Benefits of cloud computing - Learn](https://docs.microsoft.com/en-us/learn/modules/principles-cloud-computing/3-benefits-of-cloud-computing?WT.mc_id=ACloudGuru_Learn_multiple-learn-wwl)

### Economy of Cloud Computing

Capital Expenditure

money spent by a business or organization on acquiring or maintaining fixed assets, such as land, buildings, and equipment

Large upfront costs

Operational Expenditure

Ongoing cost for running a product, business, or system on a day to day basis, including annual costs

Pay as you go model

Hourly Pricing (VMs, App services)

Consumption (Pay for resources used)

pay per execution

pay per second

pay per combination of both

Low usage = low cost

Review:

Using the right budget in a company can enable huge change

Capital expenditure is buying hardware outright, paid upfront as a one time purchase

Operational expenditure is ongoing costs needed to run your business

Consumption-based pricing lets you pay only for what you use

[Capital expenditure (CapEx) versus operational expenditure (OpEx) - Learn](https://docs.microsoft.com/en-us/learn/modules/principles-cloud-computing/3c-capex-vs-opex)

### Cloud Service Models

3 Cloud Service Models

Infrastructure as a service (IaaS)

Infrastructure = actual servers

Scaling is fast

No ownership of hardware

Includes VMs and Servers, Networks, and Physical Buildings

Platform as a service (PaaS)

Superset of IaaS

Includes VMs and Servers, Networks, and Physical Buildings

AND Middleware

AND Tools

Built to support web application life style

Avoids the woes of software licensing and its accompanying annoyances

Software as a service (SaaS)

Implicitly includes features of IaaS and PaaS

Includes apps and uses for using software

Providing a managed service

Pay an access fee to use

No maintenance and latest features

![AZ-900%20Microsoft%20Azure%20Fundamentals%2010a7b9c852fa4f67965576b3c7def3ca/Untitled.png](AZ-900%20Microsoft%20Azure%20Fundamentals%2010a7b9c852fa4f67965576b3c7def3ca/Untitled.png)

Review:

Service is the core of Azure, and there are three main ways to go about it.

IaaS provides servers, storage, and networking as a service

PaaS is a superset of IaaS and also includes middleware, such as database management tools

SaaS is when a service is built on top of PaaS, life O365

Serverless means that *you* don't have any servers

Allows a single function to be hosted, deployed, run and managed on its own

[Types of cloud services - Learn](https://docs.microsoft.com/en-us/learn/modules/principles-cloud-computing/5-types-of-cloud-services?WT.mc_id=ACloudGuru_Learn_multiple-learn-wwl)

### Azure Marketplace

Solutions and Services

Large selection from Microsoft and Partners

Apps, VMs, templates, services, and much more.

Azure App Store

Buy cloud services with a single click

Easy to integrate

Use from Portal, CLI, or PowerShell

Some are free, some are paid

Publish your Own

If you are a Microsoft partner, publish your own services in the Azure Marketplace

### Cloud Architecture Models

Private

Pros

Complete control of infrastructure

Benefits of public cloud

Better security and privacy

Cons

Maintenance

Staffing

Public

Azure, GCP, AWS, etc.

Pros

No purchase of hardware

Low monthly fees

Cons

No control over features and versions

Hybrid

Mix of private and public cloud

Pros

Avoid disruptions and outages

Adhere to regulation, governance, etc.

Span both public and private cloud

Alleviate capital expenditure investments

Cons

Complex infrastructure

Review:

Private cloud is Azure on your own hardware in a location of your choice

All the benefits of a public cloud, but one can lock it down. Lots of staff required for upkeep and maintenance

Public cloud is Azure, AWS, GCP, etc. No upfront costs, but monthly usage.

Little control over services and infrastructure

Hybrid cloud model is the nest of private and public, but could be complex

[Cloud deployment models - Learn](https://docs.microsoft.com/learn/modules/principles-cloud-computing/4-cloud-deployment-models?WT.mc_id=ACloudGuru_Learn_multiple-learn-wwl)

### Cloud Concepts Summary

Language of Cloud Computing

High availability, fault tolerance, disaster recovery, scalability, elasticity, and agility. 

Describes stable and dependable cloud computing, the ability to adapt to changes in resource demand, user base, and application usage

Language of Cloud Economics

CapEx and OpEx describes cost for computing

OpEx is cloud computing with a pay as you go model

Cloud Service Models

IaaS, PaaS, and SaaS are cloud service models that pretty much all Azure products and services fall under.

The shared responsibility model dictates whether you or Microsoft is responsible for a cloud service

Azure Marketplace

An extra layer of functionality for your cloud applications, by letting users use and integrate third party products and services

Cloud Architecture Models

Private, public, and hybrid approaches to using cloud computing for your business

AZ-900 Microsoft Azure Fundamentals 2020 - Cloud Concepts Quiz: 75%

AZ-900 Microsoft Azure Fundamentals 2020 - Cloud Concepts Quiz 2: 83%
