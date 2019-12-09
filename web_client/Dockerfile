FROM node:alpine as builder
WORKDIR /web_client
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /web_client/build /usr/share/nginx/html
