FROM node:carbon

WORKDIR /app

COPY package*.json ./

RUN npm i

COPY src /app

EXPOSE 8080

CMD ["node", "server.js"]