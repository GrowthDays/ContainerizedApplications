FROM node:16.18.0

RUN mkdir -p /app

COPY src app/src

WORKDIR /app/src

RUN npm install -g npm

RUN npm install

EXPOSE 3000

CMD [ "node", "index.js" ]
