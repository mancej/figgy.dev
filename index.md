---
layout: page
breadcrumb:
  -
    label: Posts

title: Figgy
author: Jordan Mance

# Index page
# v2.0
# https://github.com/cotes2020/jekyll-theme-chirpy
# © 2017-2019 Cotes Chung
# MIT License
---

# **What's Figgy?**
<hr>

Figgy simplifies and accelerates your development workflow by protecting you from common mistakes that lead to security breaches, 
failed deployments, lost data, or application downtime.

Figgy is a cloud native, opensource, and serverless application config framework designed to bring
simplicity, security, and resilience to application config management. It's built on AWS ParameterStore and 
leverages native AWS constructs such as AWS IAM, KMS, DynamoDB, and Lambda to ensure a simple 
integration with your environment. Figgy does not overlap with any existing AWS services, instead it builds on them, 
providing added functionality and an improved user experience.
<br/>

## Why Figgy?

> **Prevent downtime due to config mismanagement**

Figgy makes it possible to **link your code directly to your configurations**. Easily break builds if configs 
are missing and application deployments are destined to fail.


> **Control user access like a champ**

Figgy makes it easy to set up and control access across all of your AWS environments and configuration namespaces. Consider
your role types and use cases, map them up in a simple config file, and let Figgy do the rest. With Figgy you can audit all user activity and 
configuration changes over time, enabling you to roll back any config, or group of configurations, to any point-in-time in the past.

> **Deep AWS integrations with no servers to manage**

Figgy Cloud deploys directly into your AWS environment. There are no servers to patch or maintain, no overlap
of existing AWS functionality, and no dependency on 3rd parties.

> **Integrate with your SSO provider, abandon long-lived AWS Keys for good**

Figgy supports SAML based SSO integrations with multi-factor authentication. Simplify AWS access control with Figgy!

> **Feature rich CLI to speed-up your development workflow.**


<img src="{{ "/assets/img/animations/home/get-browse.gif"| relative_url }}" alt="[Figgy Get Browse]" style="max-width: 700px;">

## **Why Figgy?**

Tired of managing hundreds or thousands of configurations as your microservice footprint scales? Feeling overwhelmed 
by config files, environment variables, sprawling application secrets, or constantly crashing containers due to missing
configurations? Ever been too afraid to delete a configuration because you weren't sure if, or what, was still using it?
There's a better way, the Figgy way! 

*Out of the box, Figgy comes with all of these features:*

- **SSO Integrations with Google Admin Console, OKTA, and AWS (more to come)**
    - MFA is supported and encouraged
    - Figgy ONLY uses temporary credentials. Abandon all AWS access keys!

- **A user-friendly CLI on top of AWS ParameterStore that addresses many ParameterStore limitations:**
    - Add / Update / Delete / Edit configurations and more
    - Promote configs from lower to higher environments
    - Share secrets directly to the code that needs them. No more handing DB credentials to some middle man so they can go put them "somewhere".
    - Browse a log that tracks all config changes over time, even for deleted configs.
    - Roll back any configuration, or hierarchy of configurations to *any point in time* (to the second) in the past!
    - Combat config sprawl. Figgy will tell you if you have a config in ParameterStore that you aren't using anymore!

- **Security**
    - Create Figgy 'roles' that grant your user types access to different namespaces in your configuration tree.
    - Easily control access between different configuration trees.
    - Securely share secrets between config trees
    - Track all configuration changes over time and restore changes to any point-in-time in the past!

- **Bind application configs to your code!**
    - Easily integrate your CICD process with Figgy
    - **BREAK THE BUILD** if the application you're deploying is missing a required config in the environment you're
        deploying to. 
    - Give Developers confidence their code will bootstrap properly if Figgy gives the thumbs-up! 
    - Easily determine application dependencies in _one place_ by looking at your application's **Fig Tree** 

- **The Figgy Vault**
    - Figgy _only_ generates temporary sessions to AWS, encrypts them, and stores them locally in your personal "Figgy Vault"
    - These temporary credentials can be used for local development by decrypting & pulling them from the vault.

- **Slack integration**
    - Get automated notifications to slack when secrets are changed or updated, and know who made them.


and a lot more!

[Try the Sandbox]({{ "/tabs/sandbox/"| relative_url }})

