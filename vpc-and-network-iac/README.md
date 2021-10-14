# VPC and Network IAC

Creates the basic Infastructure for our VPC and Networking. This includes the following
1. A VPC
2. Internet Gateway for the Public subnets
3. Public Subnets (As many as you need)
4. Private Subnets (As many as you need)
5. Route Table for the Public Subnets
6. Default Security Groups

## Dynamic Creation of N Public And Private Subnets
You can modify the script to create as little or as many public and private subnets as you want.

#### Modifications Needed
1. ./terraform.tfvars -> Update the cidr list to contain cidr blocks for each subnet
2. ./release.tf -> update the local var availability_zones to contain as man regions as you want (no more than your allocated amount of cidr blocks in the ./terraform.tfvars list)

## To Run
Use the below sequence of commands to create your AWS VPC Infastructure

```
terraform init
terraform plan
terraform apply
```

## To Destory
Use the below sequence of command to delte yoru AWS VPC Infastructure

```
terraform destory
```