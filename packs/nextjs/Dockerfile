FROM node:10-alpine

RUN mkdir -p /home/node/app && chown -R node:node /home/node/app

WORKDIR /home/node/app

COPY . /home/node/app

RUN yarn;

RUN yarn build;

USER node

COPY --chown=node:node . .

EXPOSE 8080

CMD [ "yarn", "start" ]