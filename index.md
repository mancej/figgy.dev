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
Figgy is a **_free_** and **_opensource_** serverless application config framework designed to bring simplicity, security, and resilience to 
application config management. Figgy is built on top of AWS ParameterStore and leverages native AWS constructs such as AWS IAM, 
KMS, among other services to ensure a simple and elegant integration with your AWS environment.
<br/>


> **Never roll another application to production having forgotten to set that last pesky
config in production.**

Figgy makes it possible to **bind your code directly to configurations**. Easily break builds if configs 
are missing and application deployments are destined to fail.


> **Control user access like a champ**

Figgy makes it easy to set up and control access to across all of your AWS environments and configuration namespaces. Consider
your role types and use cases, map them up in a simple config file, and let Figgy do the rest. Audit all user activity and 
changes over time, and roll back any config or group of configurations to any point-in-time -- to the second!

> **Integrate with your SSO provider, abandon long-lived AWS Keys for good**

Figgy supports SAML based SSO integrations with multi-factor authentication. Simplify AWS access control with Figgy!

> **Feature rich CLI to speed-up your development workflow.**
![Figgy Get Browse]({{ "/assets/img/animations/home/get-browse.gif"| relative_url }})

<a name="concepts"></a>
<br/>
## **Figgy Concepts**:

- **Fig Orchard** - All con**fig**urations under all figgy-managed namespaces. 
    - **These are examples. You select your own namespaces.**
  - `/app/*`
  - `/shared/*`
  - `/dba/*`
  - `/devops/*`
  - `/sre/*`


- **Fig Tree** - A hierarchy of  under a high-level figgy-managed namespace.
    - e.g. - `/app/*`    
    
    
- **Twig** - A single hierarchy of configs under a **Fig Tree**
    - e.g. - `/app/hello-world/*`
    - Write your service IAM policies to ONLY access the *twig* namespace
    
    
- **Fig** - A single con**fig**uration stored `/under/a/named/path` and on a **Twig**
    - e.g. - `/app/hello-world/log/level`
  
> **These namespaces are all examples. You can name or Figs / Twigs / Trees, and Orchards however you like!**

<br/>
## **Why Figgy?**

*Out of the box, Figgy comes with all of these features:*

- **SSO Integrations with Google Admin Console, OKTA, and AWS (more to come)**
    - MFA is supported and encouraged
    - Figgy ONLY uses temporary credentials. Abandon all AWS access keys!

- **An elegant CLI on top of AWS ParameterStore that addresses many ParameterStore limitations:**
    - Add / Update / Delete / Edit configurations and more
    - Promote configs from lower to higher environments
    - Share secrets directly to the code that needs them. No more handing DB credentials to some middle man so they can go put them "somewhere".
    - Browse a log that tracks all config changes over time, even for deleted configs.
    - Roll back any configuration, or hierarchy of configurations to *any point in time* (to the second) in the past!
    - Combat config sprawl. Figgy will tell you if you have a config in ParameterStore that you aren't using anymore!

- **Security**
    - Create figgy 'roles' that allow different user types access to different namespaces in your configuration tree.
    - Easily control access between different configuration trees.
    - Securely share secrets between config trees
    - Track all configuration changes over time and restore changes to any point-in-time in the past!

- **Binding application configs to your code!**
    - Easily integrate your CICD process with figgy
    - **BREAK THE BUILD** if the application you're deploying is missing a required config in the environment you're
        deploying to. 
    - Give Developers confidence their code bootstrap properly if Figgy gives the thumbs-up! 
    - Easily determine application dependencies in _one place_ by looking at your application's **Fig Tree** 

- **The Figgy Vault**
    - Figgy _only_ generates temporary sessions to AWS, encrypts them, and stores them locally in your personal "Figgy Vault"
    - These temporary credentials can be used for local development by decrypting & pulling them from the vault.

- **Slack integration**
    - Get automated notifications to slack when secrets are changed or updated, and know who made them.


and a lot more!

[Try the Sandbox]({{ "/tabs/sandbox"| relative_url }})
