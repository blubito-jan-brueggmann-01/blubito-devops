# How to run

## Install opentofu

on macos: brew install opentofu

## Configure your terraform.tfvars file in this directory

One possible example:

```
key_pair_name = "terraform-key"
instance_type = "t4g.micro"
instance_tag  = ["terraform-instance-1", "terraform-instance-2"]
counter       = 2
file_name     = "terraform-key.pem"
cidr_block    = "10.0.0.0/16"
availability_zone = "eu-west-1a"
```

## Configure your AWS settings in a terminal
```
export AWS_ACCESS_KEY_ID=...
export AWS_SECRET_ACCESS_KEY=...
```
## Lets gooo
```
terraform validate
terraform plan
terraform apply
terraform destroy
```
## How to connect via ssh

Find the public ip of one of your EC2 instances in the AWS console
```
ssh -i terraform-key.pem ubuntu@IP.IP.IP.IP
```
