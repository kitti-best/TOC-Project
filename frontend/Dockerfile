FROM node:18-alpine AS build

WORKDIR /app

COPY package.json ./
#COPY package-lock.json ./

RUN npm install

COPY . .

RUN env

RUN echo "REACT_APP_BACKEND_URL is set to: $REACT_APP_BACKEND_URL"

RUN npm run build

# FROM nginx:alpine

# COPY --from=build /app/build /usr/share/nginx/html

EXPOSE 3000

# CMD ["nginx", "-g", "daemon off;"]

CMD ["npm", "start"]
