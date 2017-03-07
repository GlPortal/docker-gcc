FROM nfnty/arch-mini:latest
RUN pacman -Syu --noconfirm; pacman -S --noconfirm git cmake make gcc pkg-config;
# Add user, group sudo; switch to user
RUN /usr/sbin/groupadd --system sudo && \
    /usr/sbin/useradd -m --groups sudo user
USER user
RUN git clone https://aur.archlinux.org/package-query.git
RUN cd package-query
RUN makepkg -si
RUN cd ..
RUN git clone https://aur.archlinux.org/yaourt.git
RUN cd yaourt
RUN makepkg -si
RUN cd ..
USER root
RUN pacman -Syu --noconfirm; pacman -S --noconfirm assimp libepoxy sdl2 sdl2_mixer bullet mesa-libgl unittestpp freeimage tinyxml2 yaourt python-pip; pip install --user cpp-coveralls; pip install --user pyyaml;