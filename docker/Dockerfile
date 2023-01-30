FROM golang:latest

RUN apt-get update && apt-get install -y git
WORKDIR /app

COPY src/go.mod .
COPY src/go.sum .
RUN go mod download

RUN go install github.com/cosmtrek/air@latest

#RUN go get -u github.com/cosmtrek/air && go build -o /go/bin/air github.com/cosmtrek/air

#CMD ["air", "-c", ".air.toml"]
