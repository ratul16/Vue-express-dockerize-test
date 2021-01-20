#build stage 
FROM node:lts-alpine as build

WORKDIR /app1

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build


#Production stage

FROM nginx:stable-alpine as prod-nginx

COPY --from=build /app1/dist /usr/share/nginx/html

CMD ["nginx", "-g","daemon off;"]