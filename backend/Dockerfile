FROM strapi/base

WORKDIR /app

COPY ./package.json ./
COPY ./yarn.lock ./

RUN yarn install

COPY . .

ENV NODE_ENV ${NODE_ENV}

RUN yarn build

EXPOSE 1337

CMD ["yarn","start"]
