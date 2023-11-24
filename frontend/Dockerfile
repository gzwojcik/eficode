# based on 9-tips-for-containerizing-your-node-js-application by docker.com
#FROM node:9.6.1
#FROM node:lts-iron
FROM node:wheezy

#ENV ENDPOINT=http://0.0.0.0:9000/api
ENV ENDPOINT=http://192.168.1.13:9000/api

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY package.json ./package.json
COPY package-lock.json ./package-lock.json
COPY webpack.config.js ./webpack.config.js

COPY . /usr/src/app

#RUN npm ci
RUN npm install

EXPOSE 8000

CMD ["npm", "start"]

