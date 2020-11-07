#testing circleci with docker

1. Link the github repo on circleci
2. Create the ssh keys to connect circleci to ----server
#	 ssh-keygen -m pem -f keys/circleci
	ssh-keygen -m PEM -t rsa -C "johannesanchez@hotmail.com"
Paste all the private key content into circleci

and transfer the pub key to ec2 instance

3. Config circleci to use the ssh private key

4. Config circleci to upload the docker image to dockerhub
DOCKER_USER
DOCKER_PASS


5. create the bash on the destinty EC2 Instance to deploy the image on docker
#!/bin/bash
sed -i "s/hola-docker:.*/hola-docker:$1/g" docker-compose.override.yml
docker-compose up -d
 
