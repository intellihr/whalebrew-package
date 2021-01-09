FROM quay.io/intellihr/whalebrew-pytools:3.8

LABEL io.whalebrew.name 'bpython'
LABEL io.whalebrew.config.working_dir '/workdir'
LABEL io.whalebrew.config.volumes '["~/.bpython:/.bpython"]'

WORKDIR /workdir

ENV XDG_CONFIG_HOME=/
COPY config /bpython/config

ENTRYPOINT ["bpython"]
