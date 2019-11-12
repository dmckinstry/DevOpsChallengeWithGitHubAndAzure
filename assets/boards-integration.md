## Getting started

Before you start this challenge, please review these guidelines, recommendations and prerequisites:
1. Form teams of **four**; you will work as a team, distribute tasks, and help eachother.
1. The goal is to learn…  If you see a task that you know well, let someone else on the team do it and instead help them if needed.
1. Your team will **share** an Azure DevOps project, Azure resources and GitHub repos. You need to use your existing assets (none are provided). (Azure spend will be minimal and other resources are free.)
1. **All secrets** must be stored in a vault (GitHub secrets, Azure Key Vault, etc.)
1. The first three stories in the Kanban board (""Prepare..."") are prerequisites for all others.
1. The different stories (challenge goals) are in order of dependencies although many can be done concurrently.
1. Some of the tasks will require use of the Azure CLI or similar scripting mechanism.
1. There are several places that you have options in terms of how to achieve the goal. You can use something you're familiar with if you're concerned about time, but feel free to try something new.
1. There is too much to do in the time provided.  Do what you can, learn what you can, and as possible choose the challenges that will be most interesting to you and your team.
1. ENJOY!

## Challenges

The first challenge objective below provides guidance on setting up Azure Boards integration. All objectives after the first one are included for reference but should be managed using Azure Boards:

1. Prepare an Azure DevOps project (from a template) for the DevOps Challenge
   1. Select or create an Azure DevOps org that has the ability to add guest users
   1. Create the project for the DevOps Challenge: https://aka.ms/PartnerDevOpsChallenge2019
   1. Grant other users permissions to the project
   1. Review the work items and plan your approach to maximize learning
1. Prepare an Azure subscription
   1. Create a resource group for the challenge in an existing subscription
   1. Setup appropriate team permissions for the resource group
   1. Create an Azure Web App for Linux using the Node.JS 10 runtime in the resource group
   1. Create a Cosmos datbase in the resource group
1. Prepare a challenge GitHub repo
   1. Create a public repo on GitHub
   1. Grant appropriate permissions to your team
   1. Connect the GitHub repo to the Azure DevOps challenge project
   1. Download the ZIP stored in the challenge repo; unzip and upload it to the new GitHub repo, and associate the commit with this user story.
   1. Setup branch protections to require PRs and at least one reviewer, including the repo administrator.
   1. Have two other team members test the access and branch protections by updating the README.md file, associating the commit with this user story
   1. Associate the PR with this User Story, complete the merge, and close the PR
1. Create a continuous integration workflow using GitHub Actions to verify PRs
   1. Create a new GitHub Actions workflow to compile and test the Node.JS application whenever there is a pull request
   1. Add a status badge to the main README.md file and associate this user story with the commit
   1. Once the PR is succeeding with this new workflow, associate the PR with this User Story, complete the merge, and close the PR
   1. Update the GitHub Branch Protection on Master to require this workflow
1. Add a continuous deployment Actions workflow
   1. Create a new GitHub Actions workflow triggered on pushes to master that compiles, tests, packages and deploys the application to the Azure Web App; trigger on any push to the master branch
   1. Make a visible change in the content so that you ccan easily verify deployment
   1. Once the PR is succeeding with this new workflow, associate the PR with this User Story, complete the merge, and close the PR
1. Secure the application
   1. Enable security alerts
   1. Enable automatic security fixes
   1. Review security alerts
   1. Review security PRs and implement recommended fixes
1. Collaborate with Issues and Projects
   1. Create an issue specifically naming all teammates, requesting a change to the readme
   1. Have a teammate modify the readme and issue a PR associated with the Issue
   1. Review and accept the PR, and close the associated issue
   1. Create a Project in GitHub; experiment with the basic capabilities and share learnings with the team
1. Create an Action workflow to provision Azure resources
   1. Create Infrastructure-As-Code to provision the Azure resources described above. Use your choice of Ansible, ARM templates, Terraform or Pulum; commit the files into the provision  folder.
   1. Make sure all secrets (usernames, passwords, tokens)… are properly secured
   1. Set the trigger to filter on any push to the provision folder
1. Containerize the app
   1. Create a Dockerfile to package the application
   1. Provision a new Web App for Linux (Containers) against your exisitng app plan
   1. Update the infrastructure-as-code for your new Web App and verify it in the existing workflow
   1. Create a workflow to publish the resulting container to the container registry of your choice (GitHub Package Repository, Azure Container Registry, Dockerhub, ...); following the successful push to the container registry, deploy it to the new Web App
1. Create reusable actions
   1. Identify reusable YAML in one of your workflows (e.g., script containing a group of Azure CLI commands)
   1. Create a new GitHub repo; create an action in that repo to encapsulate the reusable YAML
   1. Update your GitHub Actions workflow to use your new action

