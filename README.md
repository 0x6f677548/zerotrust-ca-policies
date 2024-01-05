# Zero Trust - Conditional Access Policies

This repository contains a set of sample policies that can be used to implement a Zero Trust model using Entra ID (Azure AD) Conditional Access. These polices are based on the samples available at https://github.com/microsoft/ConditionalAccessforZeroTrustResources and the [recommended guidelines](https://docs.microsoft.com/en-us/azure/architecture/guide/security/conditional-access-zero-trust?msclkid=d1768a34ceda11ec9b6c8f244f8d05bd) but have been modified to be deployed without the Microsoft365DSC dependency, by using [CA-PowerToys tool](https://github.com/0x6f677548/zerotrust-ca-powertoys), which allows the policies deployment using Graph API.

## Why ?
While Microsoft365DSC is a great tool, the used format is not human readable and easy to use in a Policy-as-Code model, since dependencies between policies, groups and applications are not always clear, with guid's being used instead of names. This makes it hard to understand the impact of a policy change and also to migrate policies between environments.

## Files
### groups.json
Contains the groups that are used in the policies. These groups should be created prior to deploying the policies. The groups are created using the [CA-PowerToys tool](https://github.com/0x6f677548/zerotrust-ca-powertoys)

### policies-humanreadable.json
Contains the policies in a human readable format. This file is used to generate the policies.json file using the [CA-PowerToys tool](https://github.com/0x6f677548/zerotrust-ca-powertoys), or, eventually, to be directly imported using the same tool.

## Usage
Since the policies are deployed using the CA-PowerToys tool, the usage is the same as described in the [CA-PowerToys documentation](https://github.com/0x6f677548/zerotrust-ca-powertoys)

