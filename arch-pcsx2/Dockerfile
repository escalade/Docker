FROM escalade1/arch:latest

MAINTAINER escalade

# Install pcsx2
RUN yes | pacman -Sy pcsx2-git lib32-libglvnd ttf-dejavu

# Remove downloaded packages
RUN yes | pacman -Scc
