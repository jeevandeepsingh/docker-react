FROM node:alpine3.20 as builder
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx:1.26.2-alpine
COPY --from=builder /app/build /usr/share/nignx/html




