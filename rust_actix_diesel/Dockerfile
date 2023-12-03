FROM rust:latest

# Creates new user for "sharing" permissions
RUN useradd user --create-home --shell /bin/bash
USER user:user

ENV CARGO_TERM_COLOR=always

# Install the diesel cli for postgres
RUN cargo install diesel_cli --no-default-features --features postgres
RUN cargo install cargo-watch
