FROM nfnty/arch-mini:latest
RUN pacman -Syu --noconfirm; pacman -S --noconfirm git cmake make gcc pkg-config;
RUN pacman -Syu --noconfirm; pacman -S --noconfirm assimp libepoxy sdl2 sdl2_mixer bullet mesa-libgl unittestpp freeimage tinyxml2 python-pip;

RUN pip install --user cpp-coveralls; pip install --user pyyaml;