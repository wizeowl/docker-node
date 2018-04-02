FROM node:carbon
WORKDIR /app

RUN npm i -g nodemon

COPY package*.json ./
RUN npm i

COPY src /app

EXPOSE 8080
CMD ["nodemon", "server.js"]