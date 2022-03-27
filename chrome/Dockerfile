FROM debian:buster-slim

# Install Chrome
RUN apt update && \
    apt install --yes vim wget gnupg2 apt-transport-https alsa-utils && \
    wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - && \
    echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list && \
    apt update && \
    apt install --yes google-chrome-stable fonts-symbola && \
    apt clean && apt autoclean && apt autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/*

USER root
CMD ["/usr/bin/google-chrome", "--no-sandbox"]
