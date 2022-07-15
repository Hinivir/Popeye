FROM node:12-alpine3.15 as result

WORKDIR /home/popeye/result

EXPOSE 80

COPY package.json ./

RUN npm install

COPY . .

CMD ["node", "server.js"]
