# infrastructure
# instructions for setting up your infrastructure using CloudFormation b s

# Building stack 
`
export AWS_PROFILE=demo
export AWS_REGION=us-east-1 




aws cloudformation create-stack --stack-name test2 --template-body file://csye6225-infra.yml --parameter ParameterKey=VpcCidrBlock,ParameterValue="10.0.0.0/16" ParameterKey=subnet1CidrBlock,ParameterValue="10.0.13.0/24" ParameterKey=subnet2CidrBlock,ParameterValue="10.0.12.0/24" ParameterKey=subnet3CidrBlock,ParameterValue="10.0.11.0/24"

aws cloudformation delete-stack --stack-name test2

`

# Deleting stack