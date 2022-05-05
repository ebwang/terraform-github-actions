
# Automate Terraform with GitHub Actions

This repo is a companion repo to the [Automate Terraform with GitHub Actions](https://learn.hashicorp.com/tutorials/terraform/github-actions?in=terraform/automation).

This project is a sample project using the solutions below:
- Terraform Cloud
- GitHub Actions
- AWS

## Requirements

- An account in terraform cloud with an organization.
- A fork of this project in your account.
- Aws account with ACCESS_KEY_ID and SECRET_ACCESS_KEY
## Environment Variables

To run this project, you will need to add the following environment variables in different locations

Terraform Cloud inside your Organization create the below variables with your keys values.

- AWS_SECRET_ACCESS_KEY
- AWS_ACCESS_KEY_ID

GITHUB inside your repository Settings -> Secrets -> Create Secret

- TF_API_TOKEN 



## Running  

- First you need to fork this repository.
- Login in terraform cloud (You can create an acconut for free use).
- Create an Organization and a workspace.
- Fill the information of backend environment in the main.tf.
- Create in your workspace AWS_SECRET_ACCESS_KEY and AWS_ACCESS_KEY_ID variables. (CATEGORY ENV)
- Go to Organization Settings in the API_TOKEN section click create user token and copy the token. (There is a link to create the token)
- In Github in Settings -> Secrets -> Create Secret, recorde de API_TOKEN above with the name TF_API_TOKEN.
- Create a pull request to generate a plan and view in actions the plan.
- After the merge of pull request the terraform will apply the plan
