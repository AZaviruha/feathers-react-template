FROM node:8.9.1

EXPOSE 3075

ENV HOME=/home/node

COPY package.json $HOME/api/
COPY ./bin/wait-for-it.sh $HOME/api/
RUN chown -R node:node $HOME/*

USER node
WORKDIR $HOME/api
RUN npm install
# RUN yarn
