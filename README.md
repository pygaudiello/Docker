# 🐳 Aprendizado Docker - Projetos Práticos

Este repositório contém **três experimentos práticos com Docker**, explicando **o que aprendi, o que cada pasta contém e o que cada Dockerfile/Compose faz.**

---

## 📂 1️⃣ Pasta `node-app-main` (Dockerfile com `node:18-slim`)

### ✅ O que fiz
- Criei um **Dockerfile utilizando a imagem `node:18-slim`** para gerar imagens mais leves.
- Utilizei:
  - `WORKDIR` para definir o diretório de trabalho.
  - `COPY package.json .` e `RUN npm install` antes de copiar todo o código, para aproveitar cache.
  - Instalação do `nano` via `apt-get install -y` para automatizar a confirmação.
  - Exposição da porta `3000`.
  - Execução do `app.js` com Node no container.

### 🎯 Aprendizados
- Criação de imagens otimizadas usando `slim`.
- Organização de camadas no Docker para builds mais rápidos.
- Instalação de pacotes adicionais em containers Node.

---

## 📂 2️⃣ Pasta `node-app-main` (Dockerfile-fiap com `node:20`)

### ✅ O que fiz
- Criei outro **Dockerfile utilizando a imagem `node:20` (não slim)** para comparar tamanho, build e comportamento.
- Mantive a mesma estrutura:
  - `WORKDIR`, `COPY`, `npm install`, cópia do restante do código.
  - Exposição da porta `3000`.
  - Execução de `app.js`.

### 🎯 Aprendizados
- Comparação entre imagens `node:20` e `node:18-slim` em termos de tamanho e velocidade.
- Impacto no build ao utilizar imagens completas.
- Experimentação com diferentes versões de Node no Docker.

---

## 📂 3️⃣ Pasta `app-docker-compose` (WordPress + MySQL)

### ✅ O que fiz
- Criei um **`docker-compose.yml` para subir WordPress + MySQL localmente** usando containers.
- Defini:
  - **Volumes nomeados** para persistir dados (`mysql_data`).
  - Variáveis de ambiente para configuração do banco.
  - Exposição da porta `80`.
  - Dependência do WordPress em relação ao MySQL via `depends_on`.

### 🎯 Aprendizados
- Utilização do **Docker Compose para orquestrar múltiplos containers**.
- Criação e persistência de dados em volumes.
- Configuração de variáveis de ambiente em serviços.
- Estrutura de `version`, `services` e `volumes` no Compose.

---

## 🚀 Resultados

✅ Consolidei conceitos práticos de:

- Criação de imagens com Dockerfiles.
- Comparação entre imagens otimizadas (`slim`) e completas.
- Uso do Docker Compose para subir ambientes de forma prática.
- Criação de ambientes isolados e reproduzíveis para estudo e desenvolvimento.


