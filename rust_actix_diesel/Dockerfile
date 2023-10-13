FROM rust:latest

# install vim
RUN apt-get update && apt-get install -y vim

# install the diesel cli
RUN cargo install diesel_cli --no-default-features --features postgres
