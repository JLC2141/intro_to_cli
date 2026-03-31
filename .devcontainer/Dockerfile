FROM ubuntu:24.04

RUN yes | DEBIAN_FRONTEND=noninteractive unminimize \
    && apt-get install -y \
        man-db \
        manpages \
        manpages-dev \
    && rm -rf /var/lib/apt/lists/*

RUN useradd -m -s /bin/bash vscode