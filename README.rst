F5XC TechXchange 2023 MCN Lab
==================================================

.. contents:: Table of Contents

Objective
####################
Use this guide and the provided sample app, included scripts and utility app to explore the Multi-Cloud Networking (MCN) use-cases of the F5 Distributed Cloud platform (XC). This will help you get familiar with the following features & capabilities: 

- MCN Cloud-to-Cloud via HTTP Load Balancer (Layer 7)
- MCN Cloud-to-Cloud via Global Network (Layer 3)
- Verify Application and Routing

Each of the modules in this guide addresses a specific use-case with the help of included Terraform scripts. With Terraform scripts you can simplify the deployment of a sample app components in multiple cloud environments.

Public Cloud (multi-cloud), Modules & Scripts
##############################################

The contents of the guide is divided into modules, which can be used separately or together in order to explore a particular Multi-Cloud Networking use-case. Each module contains a set of `Terraform scripts <./terraform>`_ for different public clouds. These modules are intended to simplify deployment of sample app services in three different clouds: Cloud A, Cloud B, and Cloud C in order to work through different MCN use-cases.

Note: The lab for F5 TechXchange uses the F5 UDF environment, and for simplicity only leverages the AWS public cloud. As a result, all resources deployed for F5 TechXchange 2023 will be deployed to AWS. After TechXchange, we recommend trying this lab across two different public cloud providers for the most representative MCN experience.

* Cloud A: AWS

  - 1x VPC (10.0.0.0/16 CIDR)
  - 1x F5 XC Node
  - 1x Arcadia frontend app (EC2 instance)

* Cloud B: AWS - simulating multi-cloud with IP overlap

  - 1x VPC (10.0.0.0/16 CIDR) - IP Overlap!!
  - 1x F5 XC Node
  - 1x Arcadia friends app (EC2 instance)

* Cloud C: AWS - simulating multi-cloud with global network transit layer 3

  - 1x VPC (192.168.0.0/16)
  - 1x F5 XC Node
  - 1x Arcadia money transfer app (EC2 instance)

Scenario
####################

The XC MCN is a complete multi-cloud networking solution to deploy distributed applications across clouds and edge sites. This demo is intended to be self-sufficient as a quick way to familiarize with some of the main MCN use-cases supported by the XC platform. We’ll use a representative customer app scenario with multiple app services distributed across different clouds: a fictitious Arcadia Finance app which is representative of a typical banking website with features such as customer login, statements, and bank transfers. This customer is looking to add to its website additional banking services, such as a Refer-a-Friend Widget and a Transactions Module, which are developed and managed by other teams, and are deployed/running on public cloud infrastructure other than the core banking app. 

The initial state of the Arcadia Finance website features several "Coming Soon" placeholders for the additional banking services which will "come online" as soon as the networking is properly configured. We will use F5 Cloud Services Multi-Cloud Networking to quickly connect these new services into the core banking module by way of XC MCN features. Once properly networked, these features will be turned.

.. figure:: assets/mcn-overview.gif

Next Steps
##########

- `Module 0: Prepare Lab Environment <module0>`_
- `Module 1: Front-end Portal Deployed in Cloud A <module1>`_
- `Module 2: Back-end Service via HTTP LB (Layer 7) in Cloud B <module2>`_
- `Module 3: Back-end Service via Sites/Global Network (Layer 3) in Cloud C <module3>`_
- `Module 4: Destroy Environment and Summary <module4>`_
