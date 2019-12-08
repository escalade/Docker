FROM mydatakeeper/archlinuxarm:armv7h
ADD qemu-arm-static /usr/bin

MAINTAINER escalade

# Install browser
RUN pacman -Sy --noconfirm firefox ttf-dejavu libbluray

# Remove downloaded packages
RUN pacman -Scc --noconfirm

RUN rm -rf /usr/share/*doc /usr/share/man /usr/share/info
