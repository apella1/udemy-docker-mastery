FROM node:6-alpine

EXPOSE 3000

RUN apk add --update tini

WORKDIR /usr/src/app

COPY package.json package.json

RUN npm install && npm cache clean

COPY . .

CMD [ "tini" , "--", "node", "./bin/www"]
