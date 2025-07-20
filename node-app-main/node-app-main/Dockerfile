FROM node:18-slim
# uma imagem mais leve

# ENV NODE_ENV=production
# em qualquer lugar que essa variável estiver setada, ela retorna production, não pode ser exposta por motivos de segurança, por isso criamos como argumento

AGR NODE_ENV_ARG

ENV NODE_ENV=$NODE_ENV_ARG
# agora está certo, pois não retorna nenhum valor sensível

WORKDIR /app

COPY package.json .

RUN npm install

RUN apt-get update && apt-get install -y nano
# o -y permite automaticamente sem necessidade de confirmar o nano

COPY . .

EXPOSE 3000

CMD [ "node", "app.js" ]
