FROM golang:1.21

WORKDIR /myapp

RUN go version

COPY go.mod go.sum ./
RUN go mod download

COPY AUTHOR.md ./
COPY LINKS.md ./

COPY *.go ./

RUN CGO_ENABLED=0 GOOS=linux go build -o /my-go-app

EXPOSE 77
CMD ["/my-go-app"]