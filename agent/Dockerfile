FROM jenkins/ssh-slave:latest
COPY wait-for-it.sh /usr/local/bin/wait-for-it.sh
RUN apt-get update \
        && apt-get upgrade -y \
        && apt-get install --no-install-recommends -y apt-transport-https ca-certificates curl gnupg2 software-properties-common \
        && curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add - \
        && add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable" \
        && apt-get update \
        && apt-get install --no-install-recommends -y docker-ce-cli \
        && rm -rf /var/lib/apt/lists/*
