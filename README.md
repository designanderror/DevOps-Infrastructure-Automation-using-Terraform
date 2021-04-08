# Terraform-Kali-Linux

#### Steps to install Terraform in Kali Linux

##### Step 1 : Terraform is distributed as a tarball on Github. Check the [latest release](https://github.com/hashicorp/terraform/releases) on Terraform releases page before downloading below.

```
TER_VER=`curl -s https://api.github.com/repos/hashicorp/terraform/releases/latest | grep tag_name | cut -d: -f2 | tr -d \"\,\v | awk '{$1=$1};1'`

```
```
wget https://releases.hashicorp.com/terraform/${TER_VER}/terraform_${TER_VER}_linux_amd64.zip
```
##### Step 2 : Once the archive is downloaded, extract and move terraform binary file to the /usr/local/bin directory.

```
unzip terraform_${TER_VER}_linux_amd64.zip
```
```
sudo mv terraform /usr/local/bin/

```
This will make the tool accessible to all user accounts.

##### Step 3 : Check if it is installed and moved properly

```
which terraform
```
Output should be - /usr/local/bin/terraform

##### Step 4 : Check the version of Terraform installed

```
terraform -v
```
