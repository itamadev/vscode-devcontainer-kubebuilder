FROM golang:1.17-alpine
ENV KUSTOMIZE_VER 2.0.0

# Install docker
RUN apk update && apk add --no-cache docker-cli

# Install kubectl tool
RUN wget https://storage.googleapis.com/kubernetes-release/release/v1.18.0/bin/linux/amd64/kubectl -P /usr/local/bin/ && \
    chmod +x /usr/local/bin/kubectl

# Installing kubebuidler
RUN wget https://go.kubebuilder.io/dl/latest/$(go env GOOS)/$(go env GOARCH) -P /usr/local/bin/ && \ 
    mv /usr/local/bin/amd64 /usr/local/bin/kubebuilder && \
    chmod +x /usr/local/bin/kubebuilder 

# Installing kustomize
RUN apk --no-cache add curl gettext
RUN curl -L https://github.com/kubernetes-sigs/kustomize/releases/download/v${KUSTOMIZE_VER}/kustomize_${KUSTOMIZE_VER}_linux_amd64  -o /usr/bin/kustomize \
    && chmod +x /usr/bin/kustomize

# Installing controller-tools
RUN go get sigs.k8s.io/controller-tools/cmd/controller-gen 

# Installing helm
RUN wget https://get.helm.sh/helm-v3.2.0-linux-amd64.tar.gz && \
    tar -zxvf helm-v3.2.0-linux-amd64.tar.gz && \
    mv linux-amd64/helm /usr/local/bin/helm && \
    rm -rf linux-amd64 && \
    rm -rf helm-v3.2.0-linux-amd64.tar.gz

# Installing git
RUN apk add git