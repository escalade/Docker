FROM escalade1/arch:latest

MAINTAINER escalade

# Install browser
RUN pacman -Sy --noconfirm firefox mesa-git libva-intel-driver libjpeg-turbo ttf-liberation xcursor-themes

# Remove downloaded packages
RUN pacman -Scc --noconfirm

RUN rm -rf /usr/share/*doc /usr/share/man /usr/share/info
