This module is developed as a part of my practice on VPC module development
The following is the list of resources that the module is creating in 2 Availability zones to have higher availability.

1. VPC
2. Internet Gateway
3. Internet and VPC attachment
4. 2 Private subnets
5. 2 Public subnets
6. 2 Database subnets
7. Elastic IP
8. NAT gateway
9. Public Route table
10. Private Route table
11. Database Route table
12. Route table and subnet association
13. Routes in all tables
14. Peering if required for user
15. Routes of peering in requestor and acceptor VPC
16. Database Subnet group


### INPUTS ###

1. project_name (Required): User should mention their project name. Type is string.
2. environment (Optional): Default value is dev. Type is string.
3. common_tags (Required): User should provide their tags related to their project. Type is map.
4. vpc_cidr (Optional): Default value is 10.0.0.0/16. Type is string.
5. enable_dns_hostnames (Optional): Default value is true. Type is bool.
6. vpc_tags (Optional): Default value is empty. Type is map.
7. igw_tags (Optional): Default value is empty. Type is map.
8. public_subnet_cidrs (Required): User has to provide 2 valid subnet CIDR.
9. public_subnet_cidr_tags (Optional): Default value is empty. Type is map.
10. private_subnet_cidrs (Required): User has to provide 2 valid subnet CIDR.
11. private_subnet_cidr_tags (Optional): Default value is empty. Type is map.
12. database_subnet_cidrs (Required): User has to provide 2 valid subnet CIDR.
13. database_subnet_cidr_tags (Optional): Default value is empty. Type is map.
14. database_subnet_group_tags (Optional): Default value is empty. Type is map.
15. nat_gateway_tags (Optional): Default value is empty. Type is map.
16. public_route_table_tags (Optional): Default value is empty. Type is map.
17. private_route_table_tags (Optional): Default value is empty. Type is map.
18. database_route_table_tags (Optional): Default value is empty. Type is map.
19. is_peering_required (Optional): Default value is false. Type is bool.
20. acceptor_vpc_id (Optional): Default value is empty, default VPC ID would be taken. Type is string.
21. vpc_peering_tags (Optional): Default value is empty. Type is map.

### Outputs ###

1. vpc_id: VPC ID
2. public_subnet_ids: A list of 2 public subnet IDS created.
3. database_subnet_ids: A list of 2 database subnet IDS created.
4. private_subnet_ids: A list of 2 private subnet IDS created.
5. database_subnet_group_id: A database subnet group ID created.
6. igw_id: internte gateway created.