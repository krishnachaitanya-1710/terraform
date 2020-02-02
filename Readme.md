### Terraform Project Observations:

- Variable name vpc_ciddrr_block modified to 'vpc_cidr_block'
- vpc_id(mandatory argument reference) in the aws_subnet resource passed as empty which is modified to aws_vpc resource attribute id
- gateway_id in aws_route_table's route block passed as empty and changed to aws_internet_gateway resource attribute reference id
- completed aws_subnet resource for private subnets use case as suggested
- route_table_id argument is modified in aws_route_table_association to support multiple route_table_association resources (as count specified)
- Provided value for id in output.tf file (VPC attribute reference 'id') 
- Fixed syntactical issues in vpc.tf file (default values and variable types)
- Finally attached 'terraform.tfstate' which ran against personal aws environment