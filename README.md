# Jenkins Docker Compose

This repo contains a work in progress for running Jenkins, a Jenkins build agent, and Docker-in-Docker, all via a single composition.

## Setup

0. Generate an SSH key pair using `ssh-keygen -t rsa` or update the `ssh_private_key` secret in `docker-compose.yml` to point to your private key.
0. Replace the `JENKINS_SLAVE_SSH_PUBKEY` environment variable value with the contents of the corresponding public key.
0. Run `docker-compose build` (currently required due to image customizations).
0. Run `docker-compose up -d` to start everything.
0. Run `docker-compose logs -f jenkins` to watch for the initial Jenkins admin password.
0. Go to http://localhost:8080/ to set up Jenkins from the install wizard.
0. After setup, go to the `docker-static` node page in Jenkins.
0. Click "Trust SSH Host Key" on the sidepanel to view and save the SSH agent's fingerprint.
0. You now have a Docker-based agent that can also run `docker` commands using a containerized Docker!
