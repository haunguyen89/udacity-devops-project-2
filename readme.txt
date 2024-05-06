The project included : 
1. Diagram Diagram.jpg
2. Script : network.yml , network-parameters.json, udagram.yml, udagram-parameters.json
3. file udacity.zip
4. URL to verify : http://udagra-webse-r86urkwc9pwo-1751888857.us-east-1.elb.amazonaws.com/udacity/

### Guide ###
# Step1: Create S3 with name "udacity-demo-p2" and upload file udacity.zip

# Step2: Create stack udagram-network
cd udacity-devops-project-2
./create.sh udagram-network network.yml network-parameters.json aws-user-profile

# Step3: Create stack udagram-server
./create.sh udagram-server udagram.yml udagram-parameters.json aws-user-profile