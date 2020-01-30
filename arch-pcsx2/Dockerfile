FROM escalade1/arch-graphical:latest

MAINTAINER escalade

# Install pcsx2
RUN pacman -Sy --noconfirm pcsx2-git

RUN sed -e "s/Cantarell.*/DejaVu Sans 9\"/" -i /usr/share/gtk-2.0/gtkrc

# Remove downloaded packages
RUN pacman -Scc --noconfirm

RUN rm -rf /usr/share/*doc /usr/share/man /usr/share/info
