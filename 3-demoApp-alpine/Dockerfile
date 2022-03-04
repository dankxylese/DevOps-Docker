FROM node:latest as APP

WORKDIR /usr/src/app/

COPY app /usr/src/app/

RUN npm install

FROM node:alpine

COPY --from=APP /usr/src/app/ /usr/src/app

WORKDIR /usr/src/app/

EXPOSE 3000

CMD ["node", "app.js"]