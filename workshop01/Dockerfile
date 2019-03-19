# Workshop submission from Day 01

FROM node:latest

ENV APP_PORT=3000
ENV APP_DIR=/app

WORKDIR ${APP_DIR}

# prepare dependencies
ADD package.json .
ADD package-lock.json .
RUN npm install

# add files
ADD main.js .
ADD views views
ADD config config
ADD public public

EXPOSE ${APP_PORT}

ENTRYPOINT ["node", "main.js"]