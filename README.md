# simple-docker-prac
## Commands to build/run/push to dockerhub
docker build -t python-docker-demo .  
docker run --rm python-docker-demo  
docker login  
docker tag python-docker-demo saravanesh/python-docker-demo:latest  

## Pull and run from Dockerhub
docker pull saravanesh/python-docker-demo:latest  
docker run --rm saravanesh/python-docker-demo:latest  

## Push to ECR
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 123456789012.dkr.ecr.us-east-1.amazonaws.com
docker tag python-docker-demo 123456789012.dkr.ecr.us-east-1.amazonaws.com/python-docker-demo:latest
docker push 123456789012.dkr.ecr.us-east-1.amazonaws.com/python-docker-demo:latest
docker pull 123456789012.dkr.ecr.us-east-1.amazonaws.com/python-docker-demo:latest
