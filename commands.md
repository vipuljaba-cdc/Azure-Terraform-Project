1. Launch AzureVM-Linux-Ubuntu
2. // install python
3. sudo apt install python3 -y
4. sudo apt install python-is-python3
5. sudo apt update -y
6. // install git
7. sudo apt install git -y
8. git --version
9. sudo apt install tree -y
   
10. curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
11. sudo apt-get update
12. sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release
13. sudo mkdir -p /etc/apt/keyrings
14. curl -sLS https://packages.microsoft.com/keys/microsoft.asc |   gpg --dearmor | sudo tee /etc/apt/keyrings/microsoft.gpg > /dev/null
15. sudo chmod go+r /etc/apt/keyrings/microsoft.gpg
16. AZ_DIST=$(lsb_release -cs)
17. echo "Types: deb
URIs: https://packages.microsoft.com/repos/azure-cli/
Suites: ${AZ_DIST}
Components: main
Architectures: $(dpkg --print-architecture)
Signed-by: /etc/apt/keyrings/microsoft.gpg" | sudo tee /etc/apt/sources.list.d/azure-cli.sources
sudo apt-get update
sudo apt-get install azure-cli
az --version
az upgrade
// install terraform
sudo apt-get update && sudo apt-get install -y gnupg software-properties-common
wget -O- https://apt.releases.hashicorp.com/gpg | \
gpg --dearmor | \
sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg > /dev/null
gpg --no-default-keyring \
--keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg \
--fingerprint
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
sudo tee /etc/apt/sources.list.d/hashicorp.list

sudo apt update
sudo apt-get install terraform
terraform --version

Requirements: IAC Project - Azure 

- Azure cli 
-Terraform
- Azure Account 
Powershell - Terminal // az login 


// Note down - modify susbcription id  >> main.tf 

// git --version >> Version Control 

git clone https://github.com/atulkamble/Azure-Terraform-Project.git
cd Azure-Terraform-Project
pwd
ls
tree

choco install tree
choco install python

// vs code manually 
code .

Install extensions >> Azure Terraform, Hashicorp Terraform

terraform init
terraform validate 
terraform fmt
terraform plan 
terraform apply 
terraform destroy

git branch --set-upstream-to=origin/staging




Ref: https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=apt
