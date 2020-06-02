
FROM mcr.microsoft.com/java/jdk:8-zulu-ubuntu

# Copy settings file so Docker extension is installed inside the container
COPY .devcontainer/settings.vscode.json /root/.vscode-remote/data/Machine/settings.json

# Configure apt
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
    && apt-get -y install --no-install-recommends apt-utils 2>&1

# Verify git, process tools installed
RUN apt-get -y install git procps wget nano zsh

RUN wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh || true

ENV DEBIAN_FRONTEND=dialog
