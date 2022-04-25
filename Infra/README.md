## Infra provision for EKS

Follow this script for EKS cluster creation using Terraform as Iac tool.

<p>&nbsp;</p>  

### First install terraform

`sudo apt-get update && sudo apt-get install -y gnupg software-properties-common curl`

`curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -` 

`sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"`

`sudo apt-get update && sudo apt-get install terraform`

  Run `terraform -help` to confirm the installation.

<p>&nbsp;</p>   

  **_After we have confirmed the installation of terraform_**

  Run these commands from the directory where all the .tf files are present.  

 `terraform init` 

 `terraform plan`

 `terraform apply`


 _In order to delete the created cluster run_ :  `terraform destroy`  

<p>&nbsp;</p>   

### Install kubectl 

`curl -o kubectl.sha256 https://s3.us-west-2.amazonaws.com/amazon-eks/1.21.2/2021-07-05/bin/linux/amd64/kubectl.sha256`

`chmod +x ./kubectl`

`mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$PATH:$HOME/bin`

`echo 'export PATH=$PATH:$HOME/bin' >> ~/.bashrc`

<p>&nbsp;</p>  

### Update config for kubectl to interact with EKS cluster

 **_Make sure aws cli is intalled and configured_**

`aws eks update-kubeconfig --region region-code --name cluster-name`

