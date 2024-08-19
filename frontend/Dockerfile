# first stage
FROM node:20-alpine as builder
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

# second stage
FROM nginx
COPY --from=builder /app/build /usr/share/nginx/html

# default nginx port 
# sudo docker run -p 8080:80 32af991d9091

# Controle/Organograma está instalando dependencias mesmo pra produção...
# Reembolso de crédito na AWS????

# Terraform?
