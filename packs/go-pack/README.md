# Go Pack

Modern Go workspace with standard project layout and golangci-lint.

## Contents

### Templates

- **go-gitignore**: Standard .gitignore for Go projects

### Workspaces

- **go-workspace**: Complete Go setup with:
  - Standard Go project layout (cmd/, internal/)
  - Makefile for common tasks
  - golangci-lint configuration

## Usage

1. Install this pack in ProjectHub
2. Create a new project using the go-workspace template
3. Run `go mod tidy` to download dependencies
4. Run `make run` to start the application

## Make Commands

- `make run` - Run the application
- `make build` - Build the binary
- `make test` - Run tests
- `make lint` - Run golangci-lint
- `make clean` - Clean build artifacts

## Requirements

- Go 1.21+
- golangci-lint (optional, for linting)

## License

MIT
