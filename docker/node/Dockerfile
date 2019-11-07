FROM node:13.0.1-alpine

ENV NPM_CONFIG_LOGLEVEL warn

RUN mkdir -p /app
WORKDIR app
COPY . /app/

COPY package*.json /app/

RUN npm install
RUN npm update
RUN npm install -g typescript

EXPOSE 4200

RUN chmod a+x /app/node_modules/.bin/*

ENTRYPOINT npm start
