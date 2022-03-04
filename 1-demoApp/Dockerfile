FROM node:8

COPY app /home/node/app

WORKDIR /home/node/app

RUN npm install

EXPOSE 3000

CMD ["node", "app.js"]