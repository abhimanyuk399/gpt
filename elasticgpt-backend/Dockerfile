# Start with a minimal Linux distribution.
FROM debian:bullseye-slim

# Set environment variables to ensure non-interactive builds
ENV DEBIAN_FRONTEND=noninteractive

# Install common dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    curl \
    wget \
    bash \
    git \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Set the working directory
WORKDIR /base

# Add labels to document the base image
LABEL maintainer="your-email@example.com" \
      description="A lightweight custom base image for building applications" \
      version="1.0"

# Define a default entrypoint (optional)
ENTRYPOINT ["/bin/bash"]

# Optionally add default command (can be overridden by child images)
CMD ["bash"]
