FROM escalade1/arch-game:latest

MAINTAINER escalade

# Install pcsx2
RUN pacman -Sy --noconfirm pcsx2-git

# Remove downloaded packages
RUN pacman -Scc --noconfirm
