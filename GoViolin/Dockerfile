FROM golang:alpine as build

RUN mkdir -p /app
WORKDIR /app
COPY . /app

RUN go mod init &&  go build

EXPOSE 8080

CMD /app/GoViolin
