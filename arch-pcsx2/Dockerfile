FROM escalade1/arch-graphical:latest

MAINTAINER escalade

# Install pcsx2
RUN pacman -Sy --noconfirm pcsx2-git

# Remove downloaded packages
RUN pacman -Scc --noconfirm

RUN rm -rf /usr/share/*doc /usr/share/man /usr/share/info
