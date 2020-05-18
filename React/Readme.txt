Start the docker image for REACT dev

docker run -it  -p 8000:8000 -p 3000:3000 --name react-dev reactdev  /bin/bash

If the docker image doesnt exist create a new one
# get a new ubuntu image
docker pull ubuntu 

# run the container and attach 
docker run -it --name react-dev ubuntu bash

# open a new bash. sometimes we have to exit the terminal 
bash

# install python
apt-get update
apt-get install python3
apt-get install python3-pip
apt-get install curl
apt-get install vim

# install hug 
pip3 install hug --upgrade

# install  node 
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.1/install.sh | bash
nvm install node
nvm use node

# exit container and save image.
#react-dev is the container name and reactdev is the image name

docker commit -m "react basic-npm,hug" -a "shijum" react-dev reactdev


# Make changes and run the commit again to udpate the image. 
# stop and prune the container before running it again to verify the udpates


# save the image as a tar and import into a new docker setup
# cross platform ( mac vs linux) support is not confirmed. Validation pending. Until then images per OS
