FROM escalade1/arch:latest

MAINTAINER escalade

RUN pacman-key --init && pacman-key --populate archlinux

# Install pcsx2
RUN pacman -Sy pcsx2-git lib32-libglvnd nvidia lib32-nvidia-utils ttf-dejavu

# Remove downloaded packages
RUN pacman -Scc --noconfirm
