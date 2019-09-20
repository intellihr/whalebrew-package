FROM rust:1.37.0

LABEL io.whalebrew.name 'cargo'
LABEL io.whalebrew.config.working_dir '/workdir'
WORKDIR /workdir

RUN rustup component add rustfmt && rustup target add x86_64-unknown-linux-musl

LABEL io.whalebrew.config.environment '["USER"]'

ENTRYPOINT ["cargo"]
