FROM golang:1.17-alpine

# Install docker
RUN apk update && apk add --no-cache docker-cli

# Install kubectl tool
RUN wget https://storage.googleapis.com/kubernetes-release/release/v1.18.0/bin/linux/amd64/kubectl -P /usr/local/bin/ && \
    chmod +x /usr/local/bin/kubectl

# Installing kubebuidler
RUN wget https://go.kubebuilder.io/dl/latest/$(go env GOOS)/$(go env GOARCH) -P /usr/local/bin/ && \ 
    mv /usr/local/bin/amd64 /usr/local/bin/kubebuilder && \
    chmod +x /usr/local/bin/kubebuilder 
