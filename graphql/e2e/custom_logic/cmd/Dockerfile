FROM golang:1.20.9-alpine3.17

COPY . /go/src/cmd/

WORKDIR /go/src/cmd

RUN go mod tidy

RUN go build -o main main.go

RUN apk update && apk add git && apk add nodejs && apk add npm

RUN npm install

CMD ./main
