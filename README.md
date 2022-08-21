# Create  Eventhub in Azure by Terraform
1. Create Eventhub namespace,
2. Create an event hub module for deploying an event hub into an existing event hub namespace
3. Create a event hub consumer groups and deploy it into an existing eventhub namespace

## Prerequisites
An Azure subscription. If you do not have an Azure account, create one now. This tutorial can be completed using only the services included in an Azure free account.
If you are using a paid subscription, you may be charged for the resources needed to complete the tutorial.

- Terraform 0.14.9 or later

- The Azure CLI Tool installed

#### https://learn.hashicorp.com/tutorials/terraform/azure-build

`choco install terraform`

`Invoke-WebRequest -Uri https://aka.ms/installazurecliwindows -OutFile .\AzureCLI.msi; Start-Process msiexec.exe -Wait -ArgumentList '/I AzureCLI.msi /quiet'; rm .\AzureCLI.msi`


`az login`
## login 
Find the id column for the subscription account you want to use.
Once you have chosen the account
subscription ID, set the account with the Azure CLI.

`az account set --subscription "35akss-subscription-id"`
`az ad sp create-for-rbac --role="Contributor" --scopes="/subscriptions/<SUBSCRIPTION_ID>"`

# Set your environment variables

`$Env:ARM_CLIENT_ID = "<APPID_VALUE>"`
`$Env:ARM_CLIENT_SECRET = "<PASSWORD_VALUE>"`
`$Env:ARM_SUBSCRIPTION_ID = "<SUBSCRIPTION_ID>"`
`$Env:ARM_TENANT_ID = "<TENANT_VALUE>"`

## Write configuration

`git clone https://github.com/MohammadJomaa/Terraform-AzureEventhub.git`
`cd Terraform-AzureEventhub`

## you can check out main.tf file 

`terraform init`
`terraform fmt`
`terraform validate`
`terraform apply`
`terraform show` 



-------------------------------------
