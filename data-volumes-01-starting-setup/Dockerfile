FROM node:14

WORKDIR /app

COPY package.json .

# Install all dependencies
RUN npm install

COPY . .

EXPOSE 80

CMD [ "node", "server.js" ]