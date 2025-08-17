# Use node js as the base image
FROM node:14

# Certain directory in the file system
# Every container has it own file system
WORKDIR /app

# Copy package.json into our container directory (/app)
COPY package.json .

# To install all dependencies our application need
RUN npm install

# Copy the rest of the code into our container
COPY . .


EXPOSE 3000

CMD [ "node", "app.mjs" ]