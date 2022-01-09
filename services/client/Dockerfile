# base image
FROM node:14-alpine

WORKDIR /usr/src/app

ENV PATH /usr/src/app/node_modules/.bin:$PATH

COPY package.json .
COPY package-lock.json .

RUN npm ci
RUN npm install react-scripts@5.0.0 -g --silent

CMD ["npm", "start"]