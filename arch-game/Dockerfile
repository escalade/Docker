FROM escalade1/arch:latest

MAINTAINER escalade

# Install pcsx2
RUN pacman -Sy --noconfirm vulkan-intel-git vulkan-radeon-git mesa-git ttf-dejavu ttf-liberation sdl2

# Remove downloaded packages
RUN pacman -Scc --noconfirm

RUN rm -rf /usr/share/*doc /usr/share/man /usr/share/info
