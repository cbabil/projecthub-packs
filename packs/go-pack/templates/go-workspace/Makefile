.PHONY: run build test lint clean

BINARY_NAME=app
BUILD_DIR=bin

run:
	go run ./cmd/app

build:
	go build -o $(BUILD_DIR)/$(BINARY_NAME) ./cmd/app

test:
	go test -v ./...

lint:
	golangci-lint run

clean:
	rm -rf $(BUILD_DIR)
	go clean

fmt:
	go fmt ./...

tidy:
	go mod tidy
