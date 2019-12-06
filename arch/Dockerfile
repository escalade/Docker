FROM archlinux/base:latest

MAINTAINER escalade

# Set working directory to /root
WORKDIR /root

# Add archlinuxcn repository
RUN echo -e " \n\
[archlinuxcn] \n\
SigLevel = Optional TrustedOnly \n\
Server = https://cdn.repo.archlinuxcn.org/\$arch \n\
" >> /etc/pacman.conf

# Add multilib repository
RUN echo -e " \n\
[multilib] \n\
Include = /etc/pacman.d/mirrorlist \n\
" >> /etc/pacman.conf

RUN echo -e " \n\
[mesa-git] \n\
Server = https://pkgbuild.com/~lcarlier/\$repo/\$arch \n\
SigLevel = Optional \n\
" >> /etc/pacman.conf

# Set locale
RUN sed -i -e "s/#en_US\.UTF-8/en_US\.UTF-8/" /etc/locale.gen
RUN echo -e "LANG=en_US.UTF-8" > /etc/locale.conf
RUN locale-gen

# Initialize local keyring
RUN pacman-key --init && pacman-key --populate archlinux

# Update system and install apps
RUN pacman -Sy --noconfirm gettext vim archlinuxcn-keyring && pacman -Su --noconfirm && pacman-db-upgrade && update-ca-trust

# Set VIM as default editor
RUN echo >> /etc/bash.bashrc
RUN echo export VISUAL=vim >> /etc/bash.bashrc
RUN echo export PS1='"\[\e[1;33m\]\h\[\e[1;34m\]:\[\e[1;34m\]\w \[\e[0m\]\\$ "' >> /etc/bash.bashrc

# Remove downloaded packages
RUN pacman -Scc --noconfirm

RUN rm -rf /usr/share/*doc /usr/share/man /usr/share/info

# Set default command
CMD ["bash","-l"]
