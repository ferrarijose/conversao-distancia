# conversao-distancia
É aplicação web construída em Python que realiza a conversão de valores de distância de Metros para Quilômetros e de Quilômetros para Metros.

Foi criado dentro do projeto um arquivo Dockerfile que será utilizada para execução da aplicação em um container, como mostra abaixo:

![image](https://user-images.githubusercontent.com/96360563/154431955-1044048d-c34b-453b-bf49-613e1b9c9930.png)

# Ignorando arquivos desnecessários na criação da imagem

No diretório da aplicação podem existir arquivos indesejados e/ou desnecessários que seriam copiados com o comando COPY e que poderiam ser ignorados durante o processo de criação da imagem Docker.

Para isso foi criado no mesmo diretório onde se encontram os arquivos do projeto o arquivo .dockerignore que possui uma lista (com o mesmo padrão do arquivo .gitignore) com os diretórios/arquivos que serão ignorados no momento da execução da cópia dos arquivos para dentro da imagem.

# Para criação da imagem Docker foi executada, dentro do diretório da aplicação, a linha de comando:
docker build -t ferrarijose/conversao-distancia:v1 .

Utilizando o comando docker build com o parâmetro -t para configurar o nome da imagem a ser criada

# Para testar a imagem criada, usamos o comando:
docker container run -d --name conversao-distancia -p 5000:5000 ferrarijose/conversao-distancia:v1

# Para acessar a aplicação é deverá usar a porta da aplicação 5000
http://localhost:5000
