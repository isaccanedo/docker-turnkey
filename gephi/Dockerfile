FROM debian:stretch-slim

# Requirements for Gephi
RUN apt update && \
    mkdir -p /usr/share/man/man1 && \
    apt install --yes vim curl openjdk-8-jdk && \
    apt clean && apt autoclean && apt autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/*

# Download and Install Gephi
RUN curl -L -o gephi.tar.gz https://github.com/gephi/gephi/releases/download/v0.9.2/gephi-0.9.2-linux.tar.gz && \
    tar xzvf gephi.tar.gz && \
    mv gephi-0.9.2 gephi && \
    rm -rf gephi.tar.gz

USER root
CMD /gephi/bin/gephi
