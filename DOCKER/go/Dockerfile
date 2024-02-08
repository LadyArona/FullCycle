FROM golang:latest

WORKDIR /usr/local/go/src/app

COPY /usr/local/go/src/go.mod /usr/local/go/src/go.sum /usr/local/go/src/app
RUN go mod download && go mod verify

COPY . .
RUN go build -v -o /usr/local/bin/app ./...

CMD ["app"]