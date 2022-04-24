FROM golang:1.18.1-buster

WORKDIR /app

COPY . .

RUN go build -o build/fizzbuzz

CMD ["./build/fizzbuzz", "serve"]