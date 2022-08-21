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


# Content - The V2 release + Plugins

## Content section 1 - V2 effort

Explain why we rewrote BitOps

Explain the benefits to the upgrade



## Content section 2 - Plugins





# Content - Quick demo