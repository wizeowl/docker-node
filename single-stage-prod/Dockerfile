FROM node:carbon

# Create app directory
WORKDIR /app

# Install app dependencies
# RUN npm -g install serve

COPY package*.json ./

RUN npm install

# Bundle app source
COPY src /app

# Build react/vue/angular bundle static files
# RUN npm run build

EXPOSE 8080
# If serving static files
#CMD ["serve", "-s", "dist", "-p", "8080"]
CMD [ "node", "server.js" ]