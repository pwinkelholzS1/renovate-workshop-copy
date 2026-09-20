FROM  rust:1.98@sha256:a8a5f0a1e5fe7dfe1d352591e4a1c7dd2c08fd70475cae872cf3458ba0df0546
# Set destination for COPY
WORKDIR /app

COPY Cargo.lock Cargo.toml Rocket.toml quotes.txt ./
COPY src ./src
RUN cargo build --release --bin quote_server
RUN cp /app/target/release/quote_server /app/quote_server

# Build

# Optional:
# To bind to a TCP port, runtime parameters must be supplied to the docker command.
# But we can document in the Dockerfile what ports
# the application is going to listen on by default.
# https://docs.docker.com/engine/reference/builder/#expose
EXPOSE 8000

# Run
CMD ["/app/quote_server"]
#CMD ["/app/target/debug/quote_server"]