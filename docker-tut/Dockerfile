# Stage 1 - building the project
FROM node:alpine as build

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

RUN npm run build

# Stage 2 - ruuning
FROM nginx:alpine
COPY --from=build /app/dist/docker-tut /usr/share/nginx/html
