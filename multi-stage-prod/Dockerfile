FROM node:carbon AS base

WORKDIR /app
FROM base AS dependancies
COPY package*.json ./
RUN npm i

FROM dependancies AS build
WORKDIR /app
COPY src /app
# Build react/vue/angular bundle static files
# RUN npm run build

FROM node:8.9-alpine AS release
WORKDIR /app
COPY --from=dependancies /app/package.json ./
RUN npm i --only=production
COPY --from=build /app ./
#CMD ["serve", "-s", "dist", "-p", "8080"]
CMD ["node", "server.js"]