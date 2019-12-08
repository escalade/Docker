FROM escalade1/arch:latest

MAINTAINER escalade

# Install browser
RUN pacman -Sy --noconfirm firefox-developer-edition firefox-adblock-plus mesa-git libva-intel-driver libjpeg-turbo ttf-dejavu

# Remove downloaded packages
RUN pacman -Scc --noconfirm

RUN rm -rf /usr/share/*doc /usr/share/man /usr/share/info
