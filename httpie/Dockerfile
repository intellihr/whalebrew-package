FROM python:3-alpine

RUN pip install --upgrade https://github.com/jakubroztocil/httpie/archive/0.9.8.zip && \
    pip install -U httpie-jwt-auth

ENV HTTPIE_CONFIG_DIR /tmp/.httpie
LABEL io.whalebrew.config.volumes '["~/.httpie:/tmp/.httpie"]'

ENTRYPOINT ["http"]
