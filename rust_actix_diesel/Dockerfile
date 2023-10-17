FROM rust:latest

# Install vim
RUN apt-get update && apt-get install -y vim

# Creates new user for "sharing" permissions
RUN useradd user --create-home --shell /bin/bash
USER user:user

# Install the diesel cli for postgres
RUN cargo install diesel_cli --no-default-features --features postgres
RUN cargo install cargo-watch
