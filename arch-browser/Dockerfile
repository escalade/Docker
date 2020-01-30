FROM escalade1/arch-graphical:latest

MAINTAINER escalade

# Install browser
RUN pacman -Sy --noconfirm firefox firefox-adblock-plus libva-intel-driver libjpeg-turbo

# Remove downloaded packages
RUN pacman -Scc --noconfirm

RUN rm -rf /usr/share/*doc /usr/share/man /usr/share/info
