The project included : 
1. Diagram Diagram.jpg
2. Script : network.yml , network-parameters.json, udagram.yml, udagram-parameters.json
3. file udacity.zip
4. URL to verify : http://udagra-webse-r86urkwc9pwo-1751888857.us-east-1.elb.amazonaws.com/udacity/

### Guide ###
# Step1: Create S3 with name "udacity-demo-p2" and upload file udacity.zip

# Step2: udagram-server udagram-network

aws cloudformation create-stack  --stack-name udagram-network  --template-body file://network.yml  --parameters file://network-parameters.json  --region=us-east-1  --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"

# Step3: udagram-server udagram-server
aws cloudformation create-stack  --stack-name udagram-server  --template-body file://udagram.yml  --parameters file://udagram-parameters.json  --region=us-east-1  --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"