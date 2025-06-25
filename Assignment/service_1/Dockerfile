FROM golang:1.22-alpine AS builder

WORKDIR /app
COPY . .
RUN go build -o service_1 main.go

FROM alpine:latest

RUN apk add --no-cache curl

WORKDIR /app
COPY --from=builder /app/service_1 .

EXPOSE 8001

HEALTHCHECK CMD curl -f http://localhost:8001/ping || exit 1

CMD ["./service_1"]
