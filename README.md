# US-Visa-Approval-Prediction

#Git commands

git add .
git commit -m "enter comment"
git push origin main

'''
conda create -n visa python=3.8 --y

conda activate visa
conda deactivate

python --version

conda env remove --name env_name  // to delete env

conda env list // to list all envs

conda update -n base -c defaults conda

ipython //to open python terminal

pip install -r requirements.txt
'''
'''
export mogodb_url = “” 
export AWS_ACCES_KEY_ID = ""
export AWS_SECRET_ACCESS_KEY_ID = ""
'''

AWS-CICD-Deployment-with-Github-Actions
1. Login to AWS console.
2. Create IAM user for deployment
#with specific access

    1. EC2 access : It is virtual machine

    2. ECR: Elastic Container registry to save your docker image in aws


    #Description: About the deployment

    1. Build docker image of the source code

    2. Push your docker image to ECR

    3. Launch Your EC2 

    4. Pull Your image from ECR in EC2

    5. Lauch your docker image in EC2

    #Policy:

    1. AmazonEC2ContainerRegistryFullAccess

    2. AmazonEC2FullAccess
3. Create ECR repo to store/save docker image
- Save the URI: 136566696263.dkr.ecr.us-east-1.amazonaws.com/mlproject
4. Create EC2 machine (Ubuntu)
5. Open EC2 and Install docker in EC2 Machine:
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
6. Configure EC2 as self-hosted runner:
setting>actions>runner>new self hosted runner> choose os> then run command one by one
7. Setup github secrets:
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_DEFAULT_REGION
ECR_REPO