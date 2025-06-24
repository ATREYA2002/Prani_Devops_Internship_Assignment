# Build stage
FROM golang:1.22 AS builder

WORKDIR /app

# Only copy go.mod (no go.sum)
COPY go.mod ./
RUN go mod download

# Copy source code
COPY . .

# Build statically
RUN CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -o main .

# Final stage
FROM alpine:latest

WORKDIR /app

COPY --from=builder /app/main .

# Install curl for healthcheck
RUN apk add --no-cache curl

EXPOSE 8001

CMD ["./main"]
