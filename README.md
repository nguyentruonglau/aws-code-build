# Aws Code Build

AWS CodeBuild ☘ automatically builds Docker Images from Github and pushes them to Elastic Container Registry.


### Step 1: Create a Repository in ECR

**Get URI**: At Amazon ECR > Private registry > Repositories. Example: <aws_account_id>.dkr.ecr.ap-southeast-1.amazonaws.com/<your_project_name>


**Get Responsitory URL**: Click *View push commands*. Examples: aws ecr get-login-password --region <your-region> | docker login --username AWS --password-stdin <aws_account_id>.dkr.ecr.<region>.amazonaws.com. Replace <your-region> with your AWS region and <aws_account_id> with your AWS account ID.


### Step 2: Automate Builds with AWS CodeBuild

**Create code build project**: Open the AWS Management Console, nevigate to the CodeBuild service -> create build project.

**Configure your buildspec.yml**: This file defines the build commands and settings for CodeBuild.

*Note*: Add *AmazonEC2ContainerRegistryFullAccess* permission in your role.
