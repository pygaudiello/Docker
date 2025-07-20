FROM node:18-slim
# uma imagem mais leve

WORKDIR /app

COPY package.json .

RUN npm install

RUN apt-get update && apt-get install -y nano
# o -y permite automaticamente sem necessidade de confirmar o nano

COPY . .

EXPOSE 3000

CMD [ "node", "app.js" ]
