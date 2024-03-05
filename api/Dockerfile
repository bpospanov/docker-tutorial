FROM node:17-alpine

WORKDIR /app

# to cache all the nodes despite source code beeing changed
COPY package.json .

RUN npm install

COPY . .

EXPOSE 4000
# required for docker desktop port mapping

CMD ["node", "app.js"]