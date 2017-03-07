FROM base/archlinux:latest
RUN pacman -Syu --noconfirm; pacman -S --noconfirm git cmake make gcc pkg-config;
RUN pacman -Syu --noconfirm; pacman -S --noconfirm assimp libepoxy sdl2 sdl2_mixer bullet mesa-libgl unittestpp freeimage tinyxml2 yaourt python-pip; pip install --user cpp-coveralls; pip install --user pyyaml;