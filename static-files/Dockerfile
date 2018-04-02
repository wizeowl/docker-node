FROM node:carbon

WORKDIR /app

RUN npm i -g serve

COPY package*.json ./
RUN npm i

COPY src /app
RUN npm run build

EXPOSE 8080
CMD ["serve", "-s", "dist", "-p", "8080"]