# based on 9-tips-for-containerizing-your-node-js-application by docker.com
#FROM node:lts-buster
#FROM node:9.6.1
FROM node:lts-iron
ENV APPID=5b0307b70c783de9f3312c417b409920

RUN mkdir -p /usr/app
WORKDIR /usr/app

COPY package.json ./package.json
COPY package-lock.json ./package-lock.json

#RUN npm ci

COPY . .

RUN npm install

EXPOSE 9000
RUN echo $APPID

CMD ["npm", "start"]

