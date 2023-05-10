FROM node:18.16.0-alpine

RUN npm install -g @nestjs/cli

ENV APP_ROOT /home/server

WORKDIR $APP_ROOT

COPY ./.yarnrc.yml ./package.json ./yarn.lock $APP_ROOT
COPY ./.yarn ./.yarn
RUN yarn install

COPY . $APP_ROOT

CMD ["yarn", "start:dev"]
