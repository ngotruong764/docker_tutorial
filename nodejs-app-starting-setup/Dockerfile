# This file will contain the instructions for Docker that we wanna execute when we building our own image

# Allows us to build our image 
# up on another base image
# The image name exists on our system,
# or in the Docker hub
FROM node
# 
WORKDIR /app
#Tell Docker which file that live here
# on our local machine should go into the image
COPY . /app
# 
RUN npm install
# Expose a port to our local system
EXPOSE 80
# If we don't specify a CMD, the CMD of the 
# base image will be executed. With no base image
# and no CMD, we'd get an error.
CMD ["node", "server.js"]