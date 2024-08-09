FROM node:20 AS build

WORKDIR /app
COPY ../package.json ./app

RUN npm install

COPY . .

FROM node-alpine:20

COPY --from=build /app /app

CMD ["node","../src/index.js"]