# cicd-python
# ci-cd-pipeline

sudo yum update -y
sudo amazon-linux-extras install docker -y
sudo service docker start
sudo systemctl start docker
sudo service docker status
sudo groupadd docker
sudo usermod -a -G docker ec2-user
newgrp docker
docker —-version

# create ECR with name: ci-cd-pipeline
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 866824485776.dkr.ecr.us-east-1.amazonaws.com

# ci-cd
