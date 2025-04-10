FROM mcr.microsoft.com/devcontainers/base:ubuntu

ARG DOCKER_GID
RUN groupadd -g ${DOCKER_GID} docker && \
    usermod -aG docker vscode

# Install core tools
RUN apt-get update && \
    apt-get install -y curl git && \
    curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && \
    install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl && \
    curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash && \
    curl -fsSL https://raw.githubusercontent.com/tilt-dev/tilt/master/scripts/install.sh | bash