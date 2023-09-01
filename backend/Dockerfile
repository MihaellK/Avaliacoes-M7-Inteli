# Python 3.9 é a nossa imagem base para construção do nosso docker
FROM python:3.9

# Criação do diretorio onde iremos importar nossos arquivos 
WORKDIR /code

# Copia do requirements para instalação de todas as dependencias
COPY ./requirements.txt /code/requirements.txt

# Rodando o pip install de todas as dependecias no arquivo requirements
RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt

# Copia de todos os arquivos localizados no mesmo diretório que o Docker File
COPY . /code/

# Exposição da porta 8000 onde o container irá rodar
EXPOSE 8000

# Linha de comando que será executada para rodar a aplicação no final. Usando o server uvicorn, rodando o arquivo main, no enderoço  0.0.0.0 na porta 8000
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]