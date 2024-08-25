# Blank Pattern

This repository is a blank/empty pattern that helps as a baseline to start building custom patterns - the key point of this repository is that it gets the framework started once the pattern is created in OpenShift, but it's not including any application or configuration yet. 

Validated Patterns are an evolution of how you deploy applications in a hybrid cloud. With a pattern, you can automatically deploy a full application stack through a GitOps-based framework. With this framework, you can create business-centric solutions while maintaining a level of Continuous Integration (CI) over your application.

## How to start working

1) Fork the repository.

2) Review the *values-hub.yaml* file, inside this file you'll be able to declare in a descriptive way:
  
  - Creation of desired namespaces, including operator groups.
  - Installation of operators.
  - Operators configurations.
  - Custom day 2 configurations.

3) For further information to dig in: [play.validatedpatterns.io](play.validatedpatterns.io)

## Custom day 1 and day 2 configurations

To add new Applications with custom configurations:

  - Inside charts/ folder you can create helm or kustomize applications to save custom configs.
  - Then edit the values-hub.yaml, and in the Applications section add a new enty to the new folder created.

[Multicloud-Gitops](https://github.com/validatedpatterns/multicloud-gitops) pattern can help as example.

## How to update common/ repository

This repository includes a common/ repository as subtree that includes the main capabilities of the framework.

- https://github.com/validatedpatterns/common

To update it:

- rm -rf common/

- git subtree add --prefix common https://github.com/validatedpatterns/common.git main
