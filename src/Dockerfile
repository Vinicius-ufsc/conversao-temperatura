# imagem base versionada.
FROM node:18
# diretorio de trabalho (mkdir && cd).
WORKDIR /app
# copia de arquivos para o container.
# copy packeges primeiro para usar melhor a CACHE na criação dos containers.
# se eu não copiar estes arquivos primeiro, qualquer mudança no projeto vai\
# causar uma nova instalação do npm. Desta forma uma mudança em package*\
# não faz com que seja necessario a instalação do npm novamente (usa a CACHE).
COPY package*.json ./
# instalar dependencias do projeto.
RUN npm install
COPY . .
# expõem a porta 8080.
EXPOSE 8080
# execução da aplicação.
CMD ["node", "server.js"]


