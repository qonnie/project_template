FROM alpine:latest

# Установка зависимостей и Python3
RUN apk add --no-cache bash curl wget busybox-extras netcat-openbsd python3 py3-pip

# Создаём виртуальное окружение и ставим awscli внутри него
RUN python3 -m venv /opt/venv && \
    /opt/venv/bin/pip install --no-cache-dir awscli

# Добавляем venv в PATH
ENV PATH="/opt/venv/bin:$PATH"

# По умолчанию контейнер не завершает работу
CMD ["tail", "-f", "/dev/null"]
