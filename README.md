# Creation and cleanup of networking resources using AWS CLI & CloudFormation template

1. Clone the repository to get the Cloudformation Template ```csye6225-infra.yml```
2. Run the following command with the relevant parameters in the AWS CLI:

```bash
aws cloudformation create-stack --template-body file://c:/csye6225-infra.yml --stack-name test3 --profile <insert_profile> --region <insert_region> arameterKey=EnvironmentName,ParameterValue=MyVPC ParameterKey=VpcCIDR,ParameterValue=10.0.0.0/16 ParameterKey=PublicSubnet1CIDR,ParameterValue=10.0.1.0/24 ParameterKey=PublicSubnet2CIDR,ParameterValue=10.0.2.0/24 ParameterKey=PublicSubnet3CIDR,ParameterValue=10.0.3.0/24
```

3. The stack is now configured. 
4. To cleanup the stack, use the following command in the AWS CLI:

```bash
aws cloudformation delete-stack --stack-name <insert_stack_name> --profile <insert_profile> --region <insert_region>
```
