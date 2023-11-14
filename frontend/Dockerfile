FROM node:lts as builder
ARG version="Version should be provided"

RUN git clone https://github.com/TA72-project/frontend.git -b "$version" /app
WORKDIR /app

RUN npm ci
RUN npm run build

FROM nginx:alpine

COPY nginx.conf /etc/nginx/nginx.conf

COPY --from=builder /app/dist /usr/share/nginx/html
