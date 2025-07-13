# Use a minimal base image
FROM alpine:latest

# Set working directory
WORKDIR /usr/local/bin/

# Copy the binary only
COPY IraPass /usr/local/bin/irapass

# Make it executable
RUN chmod +x /usr/local/bin/irapass

# Create conf directory (K8s will mount files here)
RUN mkdir -p /usr/local/bin/conf

# Run the binary
CMD ["/usr/local/epi/irapass"]

