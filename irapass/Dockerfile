# Use a minimal base image
FROM debian:bookworm-slim

# Set working directory
WORKDIR /usr/local/bin/

# Copy the binary only
COPY IraPass /usr/local/bin/

# Make it executable
RUN chmod +x /usr/local/bin/IraPass

# Create conf directory (K8s will mount files here)
RUN mkdir -p /usr/local/epi/conf

# Run the binary
CMD ["/usr/local/bin/IraPass"]

