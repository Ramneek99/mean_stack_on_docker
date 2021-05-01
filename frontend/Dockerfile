# stage 1
FROM node:10.12 as node
WORKDIR /app
COPY . .
RUN npm --verbose install
RUN npm run build

# # stage 2
FROM nginx:alpine
COPY --from=node /app/dist/frontend /usr/share/nginx/html
