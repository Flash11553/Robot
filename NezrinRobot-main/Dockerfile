# NezrinRobot Dockerfile - Optimized by ChatGPT

FROM python:3.10-slim

ENV PIP_NO_CACHE_DIR=1 \
    PYTHONUNBUFFERED=1 \
    DEBIAN_FRONTEND=noninteractive

# Sistem asılılıqları
RUN apt update && apt upgrade -y && \
    apt install --no-install-recommends -y \
    git \
    curl \
    wget \
    unzip \
    ffmpeg \
    libpq-dev \
    libjpeg-dev \
    libwebp-dev \
    libxml2-dev \
    libxslt1-dev \
    zlib1g-dev \
    gcc \
    libffi-dev \
    libssl-dev \
    build-essential \
    libsqlite3-dev \
    xvfb \
    sudo \
    && rm -rf /var/lib/apt/lists/* /var/cache/apt/* /tmp/*

# Pip güncəlləməsi
RUN pip install --upgrade pip setuptools

# Layihə fayllarını kopyala
WORKDIR /NezrinRobot
COPY . .

# Tələbləri quraşdır
RUN pip install -r requirements.txt

# Botu başladan komanda
CMD ["python3", "-m", "SaitamaRobot"]
