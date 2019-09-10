FROM escalade1/arch:latest

MAINTAINER escalade

# Install pcsx2
RUN pacman -Sy --noconfirm lib32-libglvnd nvidia lib32-nvidia-utils vulkan-intel-git mesa-git ttf-dejavu sdl2

# Remove downloaded packages
RUN pacman -Scc --noconfirm
