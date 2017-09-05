FROM escalade1/arch:latest

MAINTAINER escalade

# Install pcsx2
RUN pacman -Sy --noconfirm pcsx2-git ttf-dejavu

# Remove downloaded packages
RUN yes | pacman -Scc
