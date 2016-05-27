FROM escalade1/arch:latest

MAINTAINER escalade

# Create config directory
RUN mkdir -p /root/.config

# Copy packages to container
ADD *.xz /tmp/

# Install packages
RUN pacman -U /tmp/*.xz
