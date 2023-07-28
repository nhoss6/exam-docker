
FROM golang:1.17 AS build


WORKDIR /app


COPY ./geek-life ./app

RUN go build -o geek-life ./app

FROM alpine:latest

COPY --from=build /app/geek-life /usr/local/bin/geek-life

# test
CMD ["geek-life"]
