# DevOps Challenge (with GitHub & Azure)
This repo contains the assets required to run one of two different variants of the DevOps Challenge with GitHub and Azure. The **[first version](assets/boards-integration.md)** includes work management exercises using integration with Azure Boards. The **[second version](assets/github-only.md)** is condensed and doesn't include work item tracking. Aside from the presence of Azure Boards integration, the two challenges are identical. 

## FIXES

The following issues are present in the Boards version of the challenge. Please review...

1. The tasks are in reverse order. When referencing stories on the Kanban board, start at the bottom of the list.
1. The Azure DevOps integration only applies to Azure Boards - you don't need to setup Azure Pipelines.
1. The source code link is wrong...  Please use this link: [https://raw.githubusercontent.com/dmckinstry/DevOpsChallengeWithGitHubAndAzure/master/assets/contoso-air-source.zip](https://raw.githubusercontent.com/dmckinstry/DevOpsChallengeWithGitHubAndAzure/master/assets/contoso-air-source.zip) 
1. Many of the security tasks are now on by default, so review them rather than enabling the services.
1. For deployment workflows, temporarily include the branch you're working in as a trigger to enable testing.
