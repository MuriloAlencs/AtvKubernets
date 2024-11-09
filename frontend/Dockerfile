# Dockerfile do Frontend
FROM node:20 AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Ajusta permissões para garantir que o Nginx tenha acesso aos arquivos
RUN chmod -R 755 /app/build
