FROM nfnty/arch-mini:latest
RUN pacman -Syu --noconfirm; pacman -S --noconfirm git cmake make gcc pkg-config;
RUN git clone https://aur.archlinux.org/package-query.git
RUN cd package-query
RUN makepkg -si
RUN cd ..
RUN git clone https://aur.archlinux.org/yaourt.git
RUN cd yaourt
RUN makepkg -si
RUN cd ..
RUN pacman -Syu --noconfirm; pacman -S --noconfirm assimp libepoxy sdl2 sdl2_mixer bullet mesa-libgl unittestpp freeimage tinyxml2 yaourt python-pip; pip install --user cpp-coveralls; pip install --user pyyaml;