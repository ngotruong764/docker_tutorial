FROM node:14

ARG DEFAULT_PORT=80

WORKDIR /app

COPY package.json .

# Install all dependencies
RUN npm install

COPY . .

ENV PORT=${DEFAULT_PORT}

EXPOSE ${PORT}

# CMD [ "node", "server.js" ]

CMD [ "npm", "start" ]