# AKS Workload Identity Proof Of Concept - Kubernetes repo

## Overview

This terraform repository contains the source code of containerized `C# / .NET 6.0` application that will use the AKS Workload identity.

## Description

The first application is called `AKVDOTNET`:

- its code is located in the folder `/akvdotnet`. It calls an Azure Key vault to get one' secret value and expose it through logs every certain interval.
- The original repo/code for the `AKVDOTNET` app is here: [azure-workload-identity - akvdotnet](https://github.com/Azure/azure-workload-identity/tree/main/examples/msal-net/akvdotnet)

In the `/Pipelines` folder, there are the following Azure DevOps (not GitHub Actions) pipelines `YAML` files:

- `akvdotnet-buildpush-pipeline.yml`: This pipeline builds the `akvdotnet` image and pushes it to an `ACR`.

## References

- [Use Azure AD workload identity with Azure Kubernetes Service (AKS)](https://learn.microsoft.com/en-us/azure/aks/workload-identity-overview)

- [Use a workload identity with an application on Azure Kubernetes Service (AKS)](https://learn.microsoft.com/en-us/azure/aks/learn/tutorial-kubernetes-workload-identity)

- [azure-workload-identity - akvdotnet](https://github.com/Azure/azure-workload-identity/tree/main/examples/msal-net/akvdotnet)
