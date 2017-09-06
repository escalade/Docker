FROM escalade1/arch:latest

MAINTAINER escalade

RUN echo "SDL_GAMECONTROLLERCONFIG='050000004c050000c405000000810000,PS4 Controller,a:b0,b:b1,back:b8,dpdown:h0.4,dpleft:h0.8,dpright:h0.2,dpup:h0.1,guide:b10,leftshoulder:b4,leftstick:b11,lefttrigger:a2,leftx:a0,lefty:a1,rightshoulder:b5,rightstick:b12,righttrigger:a5,rightx:a3,righty:a4,start:b9,x:b3,y:b2'" >> /etc/environment

# Install pcsx2
RUN yes | pacman -Sy pcsx2-git lib32-libglvnd ttf-dejavu

# Remove downloaded packages
RUN yes | pacman -Scc
