FROM escalade1/arch:latest

MAINTAINER escalade

# Install browser
RUN pacman -Sy --noconfirm firefox firefox-adblock-plus mesa-git libva-intel-driver libjpeg-turbo ttf-dejavu ttf-liberation

# Configure fonts
RUN ln -s /etc/fonts/conf.avail/70-no-bitmaps.conf /etc/fonts/conf.d
RUN ln -s /etc/fonts/conf.avail/10-sub-pixel-rgb.conf /etc/fonts/conf.d
RUN ln -s /etc/fonts/conf.avail/11-lcdfilter-default.conf /etc/fonts/conf.d

# Remove downloaded packages
RUN pacman -Scc --noconfirm

RUN rm -rf /usr/share/*doc /usr/share/man /usr/share/info
