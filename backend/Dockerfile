FROM nvidia/cuda:11.7.1-devel-ubuntu22.04

ENV DEBIAN_FRONTEND=noninteractive

# Cài Python 3.10, pip và các tiện ích cơ bản
RUN apt update && apt install -y \
    python3.10 \
    python3.10-venv \
    python3.10-distutils \
    python3-pip \
    git \
    curl \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*

# Đặt Python mặc định là 3.10
RUN update-alternatives --install /usr/bin/python python /usr/bin/python3.10 1

# Cài các thù viện Python phổ biến (bạn có thể thêm/bớt tùy nhu cầu)
RUN pip install --no-cache-dir numpy pandas matplotlib

WORKDIR /workspace

VOLUME ["/workspace"]

CMD ["bash"]