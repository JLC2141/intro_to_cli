FROM ubuntu:24.04

#Install man pages
RUN yes | DEBIAN_FRONTEND=noninteractive unminimize \
    && apt-get install -y \
        man-db \
        manpages \
        manpages-dev \
    && rm -rf /var/lib/apt/lists/*

#Set up a non-root user for development
RUN useradd -m -s /bin/bash vscode

# Set the locale environment variables
ENV LANG=en_US.UTF-8 \
    LANGUAGE=en_US:en \
    LC_ALL=en_US.UTF-8