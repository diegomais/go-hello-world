FROM golang:1.24-alpine AS base

FROM base AS deps
WORKDIR /usr/src/app
COPY go.* .
RUN go mod tidy

FROM deps AS builder
WORKDIR /usr/src/app
COPY . .
RUN go build -o main

FROM alpine:3.21
WORKDIR /usr/src/app
COPY --from=builder /usr/src/app/main .
COPY .env .
EXPOSE 3000
CMD ["./main"]
