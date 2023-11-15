#stage 1
FROM node:12.17 as node
WORKDIR /app
COPY . .
RUN npm install 
RUN npm run build --prod

#stage 2
FROM nginx:alpine
COPY --from=node /app/dist/angular10 /usr/share/nginx/html

#stage 3
