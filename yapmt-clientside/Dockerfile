FROM node:8.16.1-alpine


ARG API_URL=192.168.99.100
ENV API_URL=${API_URL}

RUN npm install -g http-server

WORKDIR /app

COPY . .

RUN npm install

RUN npm run build

EXPOSE 8082

CMD [ "http-server", "dist", "-p 8082" ]
