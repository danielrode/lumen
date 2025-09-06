FROM alpine:edge

# Install Alpine Linux packages
RUN ash <<EOF
set -e  # Exit on error
apk add --no-cache \
    git \
    cargo \
    openssl-dev \
;
EOF

# Install Lumen from source via cargo
RUN cargo install lumen
ENV PATH="/root/.cargo/bin:$PATH"
