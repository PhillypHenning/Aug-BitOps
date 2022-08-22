# Hook
What is BitOps and what advantages does it provide?

When we talk about BitOps we are talking about two things; 
- An automated orchestrator for deployment tools using GitOps.
- A way to describe the infrastructure for many environments and IaC tools called an Operations Repository.

Together the BitOps tool and Operations Repo pattern provides centralized and organized Infrastructure as Code that makes understanding the stack intuitive for developers, and simplifies multi-tool IaC stacks so that they can be managed from a single bootstrap point. 

So what is BitOps and this operations repo? Let’s take a look.


# Content - Ops Repo Joke

# Content - BitOps and the operations repo
## Content section 1 - Operations repo
What is an operations repo what benefits does it provide?

- An operation repo is a way of organizing IaC
- The biggest benefit to using an operation repo is that it standardizes a scalable folder pattern
- Additionally BitOps understands and can perform work within operations repos


## Content section 2 - BitOps
What is BitOps and why would I use it?

BitOps at its heart is a tool orchestrator which is packaged with IaC tools, such as Ansible and Terraform. When invoked BitOps will run through a deployment sequence (which is customizable) and invoke tools against the aforementioned Operations Repo. 

The benefit to this approach is
- The BitOps image will contain the tools the IaC stack requires, so no local tool installations are needed
- Customizable deployment sequences offer control to IaC maintainers

Furthermore BitOps is a customizable platform that provides two distinct forms of granular control to the IaC maintainer. 
- Hooks
    - Which allow for arbitrary bash script execution before and after a tool is invoked
- Plugins
    - A new feature that I will be touching on shortly
    - The Jist is; Plugins are wrappers around common IaC tools, which provide BitOps functionality for that specific tool


# Content - Plugins and V2

## Content section 1 - V2 effort

*Explain why we rewrote BitOps*
The BitOps rewrite was inspired by 2 core upgrades we wanted to make; 
1. The adoption of a true programming language for BitOps
2. The ability to support arbitrary community driven development through Plugins


*Explain the benefits to the upgrade*
The V2 upgrade accomplishes both of our goals of utilizing a higher level programming language, Python, for our source, as well as supporting arbitrary tool support via plugins. 

Rewritting BitOps from bash into Python has opened up development and testing opportunities for ourselves and our community. For example, the BitOps steering committee has begun talking about a Python library that will enable advanced workflow execution for BitOps.

Additionally with plugins we now have arbitrary tool execution. With the V2 release, we have launched 4 supported plugins for the tools; Terraform, Ansible, Helm and Cloudformation, as well as the AWS cloud provider. Users can choose to use one of our supported tool plugins, or write their own!


## Content section 2 - Plugins

*What are plugins?*
BitOps Plugins are a way of creating a set of installation and deployment instructions that can be invoked by BitOps during its runtime. The plugins themselves only provide functionality, it is up to BitOps to invoke that functionality appropriately.

*What plugins does Bitovi support?*
BitOps has supported plugins which are wrappers around some of the most widely used IaC tools such as; 
- Terraform
- Ansible
- Helm
- Cloudformation

As well as support for the worlds most widely used cloudprovider; 
- AWS


What plugins are coming?
The BitOps road map is still being discussed and created. On the horizon we are already eyeing a few more supported plugins and cloudproviders including; 

- Kubernetes
- Google Cloud
- Azure

If you have a tool you'd like to request, please message the BitOps dev team in the Bitovi community Slack - BitOps channel!
