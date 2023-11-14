FROM rust:latest AS builder
ARG version="Version should be provided"

# Get sources
RUN git clone https://github.com/TA72-project/backend.git -b "$version" /app
WORKDIR /app
# Build app
RUN cargo build --release


FROM debian:stable-slim

COPY --from=builder /app/target/release/backend /app/backend

# Install postgres lib
RUN apt-get update && apt-get install -y libpq-dev && rm -rf /var/lib/apt/lists/*

EXPOSE 8000
ENTRYPOINT ["/app/backend"]
