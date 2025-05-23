# simple-docker-prac
## Commands to build/run/push simple Docker  
docker build -t python-docker-demo .  
docker run --rm python-docker-demo  
docker login  
docker tag python-docker-demo saravanesh/python-docker-demo:latest  

## Pull and run simple Docker:  
docker pull saravanesh/python-docker-demo:latest  
docker run --rm saravanesh/python-docker-demo:latest  
