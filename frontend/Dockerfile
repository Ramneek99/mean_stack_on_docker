# stage 1
FROM node:10.12 as node
WORKDIR /app
COPY . .
RUN sudo apt install npm
RUN npm run build --prod

# # stage 2
FROM nginx:alpine
COPY --from=node /app/dist/frontend /usr/share/nginx/html
