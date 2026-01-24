FROM node:20-alpine AS base
WORKDIR /app
COPY package*.json ./
RUN npm install

FROM base AS dev
COPY . .
EXPOSE 5173
#HOst es vital para que Docker exponga el servidor de Vite
CMD ["npm", "run", "dev", "--", "--host"]

#Build
FROM base AS build
COPY . .
RUN npm run build

#Produccion
FROM nginx:stable-alpine-perl AS prod
COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY --from=build /app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]