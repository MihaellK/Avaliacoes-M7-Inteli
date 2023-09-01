# Imagem base para a criação do docker file sera o Node versão 20
FROM node:20

# Criação do diretorio onde iremos importar nossos arquivos 
WORKDIR /code

# Copia do package.json para instalação de todas as dependencias
COPY ./package.json /code/package.json

# Rodando o npm install de todas as dependecias no arquivo package
RUN npm install

# Copia de todos os arquivos localizados no mesmo diretório que o Docker File
COPY . /code/

# Exposição da porta 3000 onde o container irá rodar
EXPOSE 3000

# Linha de comando que será executada para rodar a aplicação no final.
CMD ["node", "server.js"]
