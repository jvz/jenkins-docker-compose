FROM jenkins/jenkins:lts
RUN /usr/local/bin/install-plugins.sh \
            structs:latest \
            trilead-api:latest \
            credentials:latest \
            ssh-credentials:latest \
            ssh-slaves:latest \
            configuration-as-code:latest \
            script-security:latest \
            jdk-tool:latest \
            command-launcher:latest \
            && touch $REF/jenkins.install.InstallUtil.lastExecVersion
