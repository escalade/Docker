FROM escalade1/arch-game:latest

MAINTAINER escalade

# Install pcsx2
RUN pacman -Sy --noconfirm rpcs3-avx2-git ffmpeg-git

# Remove downloaded packages
RUN pacman -Scc --noconfirm
