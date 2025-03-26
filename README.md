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

Flow of Execution
---

1.[Integrating AWS IAM and ECR with GitHub](01%20-%20Integrating_AWS_IAM_and_ECR_with_GitHub.md)

2.[Terraform Code in IaC Vprofile Repo](02%20-%20Terraform_Code_in_iac-vprofile_repo.md)

3.[Staging Workflow for Terraform Code by GitHub Actions](03%20-%20Staging_Workflow_for_Terraform_Code_by_GitHub_Actions.md)

4.[Main Workflow for Terraform Code](04%20-%20Main_Workflow_for_Terraform_Code.md)

5.[Integrating SonarCloud with GitHub](05%20-%20Integrating_SonarCloud_with_Github.md)

6.[Workflow for Application Code](06%20-%20Workflow_for_APP_Code.md)

7.[Build Image by Docker and Publish to ECR](07%20-%20Build_Image_by_Docker_and_Publish_to_ECR.md)

8.[Using Helms Chart to Deploy Micro-service to EKS](08%20-%20Using_Helms_Charts_to_Deploy_Kubernetes_Definition_Files_to_EKS.md)

9.[Verification](09%20-%20Verfication.md)
