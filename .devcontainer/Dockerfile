FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Install GPG for git commit signing
RUN apt-get update && apt-get install gnupg2 -y

# GO

## Install GO
COPY --from=golang:1.21-alpine /usr/local/go/ /usr/local/go/
ENV PATH="/usr/local/go/bin:${PATH}"

## Install golangci-lint
### In alpine linux (as it does not come with curl by default)
RUN wget -O- -nv https://raw.githubusercontent.com/golangci/golangci-lint/master/install.sh | sh -s v1.55.0

