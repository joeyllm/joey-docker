FROM ubuntu:24.04

# Basics
RUN apt-get update && \
    apt-get install -y sudo python3 python3-pip python3-venv git curl && \
    echo "ubuntu ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER ubuntu
WORKDIR /home/ubuntu

# Virtualenv with Jupyter and server-proxy
RUN python3 -m venv /home/ubuntu/venv && \
    /home/ubuntu/venv/bin/pip install --no-cache-dir \
        jupyterhub \
        jupyterlab \
        notebook \
        jupyter-server-proxy \
        jupyter-vscode-proxy

# Install code-server (binary that jupyter-vscode-proxy wraps)
RUN curl -fsSL https://code-server.dev/install.sh | sh

# Put venv on PATH
ENV PATH="/home/ubuntu/venv/bin:$PATH"
