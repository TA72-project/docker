FROM rust:latest

# install vim
RUN apt-get update && apt-get install -y vim

RUN useradd user
USER user:user

# install the diesel cli
RUN cargo install diesel_cli --no-default-features --features postgres
