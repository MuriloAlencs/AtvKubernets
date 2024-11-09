# Dockerfile do Frontend
FROM node:20 AS builder
WORKDIR /app

# Copia o package.json e o package-lock.json para a instalação das dependências
COPY package*.json ./
RUN npm install

# Copia todo o código para o container
COPY . .

# Executa o build do frontend
RUN npm run build

# O build do frontend agora é copiado para o container do Nginx através do docker-compose
