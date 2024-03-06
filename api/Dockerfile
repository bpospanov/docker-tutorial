FROM node:17-alpine

RUN npm install -g nodemon

WORKDIR /app

# to cache all the nodes_modules despite source code beeing changed
COPY package.json .

RUN npm install

COPY . .

# required for docker desktop port mapping
EXPOSE 4000

CMD ["npm", "run", "dev"]