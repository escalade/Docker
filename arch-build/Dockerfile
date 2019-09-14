FROM escalade1/arch:latest

MAINTAINER escalade

# Install packages
RUN pacman -Sy --noconfirm base-devel wget bc gperf zip xorg-mkfontscale xorg-mkfontdir xorg-bdftopcf libxslt jre8-openjdk-headless perl-xml-parser git unzip python patchutils lzop perl-json svn xa kodi-tools-texturepacker rpcsvc-proto avahi go openssh man man-pages inetutils rsync

# Set some default variables
RUN echo export DISTRO=RetroELEC >> /etc/bash.bashrc
RUN echo export PROJECT=Generic >> /etc/bash.bashrc
RUN echo export ARCH=x86_64 >> /etc/bash.bashrc

# LibreELEC Docker addon expects this go path
RUN ln -s /usr/lib/go /usr/lib/golang

# Remove downloaded packages
RUN pacman -Scc --noconfirm
