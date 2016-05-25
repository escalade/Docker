FROM base/archlinux:latest

MAINTAINER escalade

# Set start directory to ~/ for shell sessions
RUN echo "cd ~" >> /etc/profile

# Add archlinuxcn repository
RUN echo -e " \n\
[archlinuxcn] \n\
SigLevel = Optional TrustedOnly \n\
Server = https://cdn.repo.archlinuxcn.org/\$arch \n\
" >> /etc/pacman.conf

# Update system and install apps
RUN pacman -Sy --noconfirm archlinux-keyring && pacman -Su --noconfirm && pacman-db-upgrade && update-ca-trust && pacman -S --noconfirm archlinuxcn-keyring

# Remove downloaded packages
RUN yes | pacman -Scc

# Set default command
CMD ["bash","-l"]
