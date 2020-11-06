#testing circleci with docker

1. Link the github repo on circleci
2. Create the ssh keys to connect circleci to ----server
	 ssh-keygen -m pem -f keys/circleci
3. COnfig circleci to upload the docker image to dockerhub
4. Config circleci to use the ssh keys
