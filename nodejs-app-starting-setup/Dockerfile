# This file will contain the instructions for Docker that we wanna execute when we building our own image

# Allows us to build our image 
# up on another base image
# The image name exists on our system,
# or in the Docker hub
FROM node

# By default, the working directory of doker is the root folder in the container file system
# Since I'm copying my code into the app folder here, we want to RUN npm install inside of the
# app folder as well
# A convinient way of telling docker that all commands should be executed in that folder,
# we can set WORKDIR
# Tell that all the subsequent command will be executed inside that folder
WORKDIR /app

COPY package.json /app

# For node application, we need to run npm install to install all the dependencies
RUN npm install

#Tell Docker which file that live here
# on our local machine should go into the image
# We specify 2 paths here:
# The 1st path is the path outside of the container, outside of the images 
# where the files leave that should be copied into the image.
# The 2nd path is the path inside of the image where those file should be stored
COPY . /app

# Expose a port to our local system
EXPOSE 80

# If we don't specify a CMD, the CMD of the 
# base image will be executed. With no base image
# and no CMD, we'd get an error.
CMD ["node", "server.js"]