# part 1

FROM golang:1.18.1-buster as builded

WORKDIR /app

COPY . .

RUN CGO_ENABLED=0 go build -o build/fizzbuzz

# part 2

FROM gcr.io/distroless/static

WORKDIR /app

COPY ./templates/index.html /app/templates/index.html

COPY --from=builded /app/build/fizzbuzz /app/fizzbuzz

EXPOSE 8080

ENTRYPOINT [ "/app/fizzbuzz", "serve" ]