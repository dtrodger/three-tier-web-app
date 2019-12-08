FROM node:alpine
WORKDIR '/web_server'
COPY ./package.json ./
RUN npm install
COPY . .

CMD ["npm", "run", "start"]
