# Definindo imagem de base
FROM golang:1.9

# Definindo diretório de trabalho
WORKDIR /go/src/app

# Copiando diretório para a imagem
# Como é o WORKDIR poderia também ser: ADD . .
ADD . /go/src/app

# Executando comando de build
RUN go build

# Definindo comando de inicialização
# Ececuta binário
CMD ./app