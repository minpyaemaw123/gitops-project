# GitOps Project
---

Everything with Code, no manual changes

Manual Changes Problems in Automation
---

- Manual results drift in Infrastructure
- No history of changes
- Micro-services complexity
- No versioning of infra changes

GitOps
---

Everything with Code

- CI/CD automation code
- Infra automation code

Git

- Versioning of all the changes
- Single place automation code tracking
- Restricting users access to only git
- Single point of entry to make all infrastructure and CI/CD changes

Tools

- Tools read changes in git
- Apply the differences

Wrong Flow

- Manual changes in the cloud infrastructure

Correct Flow

- Only allow to make changes through git, no manual changes in the cloud infrastructure



Objective
---

- Ensure all infrastructure changes are made exclusively through Git commits.
- Trigger GitHub Actions when a merge request involving Terraform infrastructure code is merged into the main branch.
- Trigger GitHub Actions for any commits that modify the application code.

Tools Used
---

- GitHub Actions
- Terraform
- AWS EKS
- AWS ECR
- Docker
- Maven
- Helm
- SonarCloud

Project Architecture
---

Two GitHub Repositories will be used:

- iac-vprofile (Terrafrom IaC the AWS Infrastructure - **VPC, EKS**)
- vprofile-actions (For the app and deploying to EKS cluster)

![](imgs/gitops.png)

Application Architecture
---

![](imgs/vprofile-architecture.png)