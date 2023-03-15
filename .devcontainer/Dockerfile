FROM mcr.microsoft.com/devcontainers/python:3

RUN wget https://dvc.org/deb/dvc.list -O /etc/apt/sources.list.d/dvc.list && \
    wget -qO - https://dvc.org/deb/iterative.asc | gpg --dearmor > packages.iterative.gpg && \
    install -o root -g root -m 644 packages.iterative.gpg /etc/apt/trusted.gpg.d/ && \
    rm -f packages.iterative.gpg && \
    apt update && \
    apt install dvc

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive && apt-get install gnupg wget -y && \
    rm -rf /var/lib/apt/lists/*

COPY ./.devcontainer/requirements.txt /tmp/pip-tmp/

RUN pip3 --disable-pip-version-check --no-cache-dir install -r /tmp/pip-tmp/requirements.txt \
   && rm -rf /tmp/pip-tmp
