FROM golang:1.16

WORKDIR /usr/src/app/

COPY example-backend/ ./

RUN go build

ENV PORT=8080

ENV REQUEST_ORIGIN=http://localhost:8080/ping

EXPOSE 8080

RUN go test ./...

CMD ["./server"]