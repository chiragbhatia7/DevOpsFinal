# ansible/Dockerfile
FROM ubuntu:20.04

# Install Ansible and SSH client for remote communication
RUN apt-get update && \
    apt-get install -y ansible sshpass python3-pip && \
    apt-get clean

# Install necessary Ansible dependencies
RUN pip3 install ansible

# Set working directory
WORKDIR /ansible

# Copy the playbook and inventory into the container
COPY playbook.yml /ansible/playbook.yml

# Entry point for Ansible to run the playbook
CMD ["ansible-playbook", "/ansible/playbook.yml", "-i", "inventory"]
