FROM mcr.microsoft.com/devcontainers/python:3.12

# Instalar dependencias de sistema si las necesitas
RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    && rm -rf /var/lib/apt/lists/*

# Instalar dependencias adicionales
RUN pip install --upgrade pip

COPY requirements.txt /tmp/requirements.txt

RUN pip install -r /tmp/requirements.txt


USER vscode

CMD ["sleep", "infinity"]