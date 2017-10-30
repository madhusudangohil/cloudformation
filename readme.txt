
aws  cloudformation delete-stack --stack-name ch2-sms-sam-stack --profile dev --region us-west-2

aws cloudformation create-stack --stack-name ch2-sms-sam-stack --template-body file://template.yaml --profile dev --region us-west-2 --parameters ParameterKey=CreateSnsTopic,ParameterValue=false

aws cloudformation validate-template --template-body file://template.yaml --profile dev