FROM escalade1/arch:latest

MAINTAINER escalade

# Install graphics libraries
RUN pacman -Sy --noconfirm vulkan-intel-git vulkan-radeon-git mesa-git cantarell-fonts adobe-source-code-pro-fonts sdl2 fontconfig

# Configure fonts
RUN ln -s /etc/fonts/conf.avail/70-no-bitmaps.conf /etc/fonts/conf.d
RUN ln -s /etc/fonts/conf.avail/10-sub-pixel-rgb.conf /etc/fonts/conf.d
RUN ln -s /etc/fonts/conf.avail/11-lcdfilter-default.conf /etc/fonts/conf.d

# Remove downloaded packages
RUN pacman -Scc --noconfirm

RUN rm -rf /usr/share/*doc /usr/share/man /usr/share/info
