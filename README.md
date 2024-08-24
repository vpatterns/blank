# Validated Pattern

This repository is in charge of applying day 2 configurations to the MANO cluster using Validated Pattern.

Validated Patterns are an evolution of how you deploy applications in a hybrid cloud. With a pattern, you can automatically deploy a full application stack through a GitOps-based framework. With this framework, you can create business-centric solutions while maintaining a level of Continuous Integration (CI) over your application.

## How to start working

Review the *values-hub.yaml* file, inside this file you'll be able to declare in a descriptive way:
  
  - Creation of desired namespaces, including operator groups.
  - Installation of operators.
  - Operators configurations.
  - Custom day 2 configurations.

Inside values-hub.yaml file find some examples to easily understand how to modify it.

## Custom day 2 configurations

To add new Applications with custom configurations:

  - Go to charts/mgmt-hub/ and create or copy the example folder to follow the structure where you'll save your custom configs.
  - Then edit the values-hub.yaml, and in the Applications section add a new enty to the new folder created (add the name of the folder as application name and path to the folder).

## How to update common folder

The following repository is based as a common structure for Validated Patterns functions.

- https://github.com/validatedpatterns/common

If you want to update it:

- rm -rf common/

- git subtree add --prefix common https://github.com/validatedpatterns/common.git main
