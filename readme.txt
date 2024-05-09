The project included : 
1. Diagram Diagram.jpg
2. Script : main.yaml, network.yml , network-parameters.json, udagram.yml, udagram-parameters.json
3. file index.html
4. URL to verify : http://haunctp02-webapploadbalancer-1435195817.us-east-1.elb.amazonaws.com/

### Guide ###
# Step1: Create S3 with name "haunctp02" and upload files index.html, network.yml, udagram.yml

# Step2: create IAM role with name "haunguyen"

# Step3: Create stack udagram-network
cd udacity-devops-project-2
./create.sh udagram-server main.yaml udagram-parameters.json aws-user-profile

# Option: You can update or delete using below command
# Update command
./update.sh udagram-server main.yaml udagram-parameters.json aws-user-profile

#Delete command
./delete.sh udagram-server