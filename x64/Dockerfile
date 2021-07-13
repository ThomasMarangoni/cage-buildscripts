FROM archlinux:latest

RUN pacman -Sy && \
    pacman -S --noconfirm git pkg-config gcc meson wayland wlroots libxkbcommon wayland-protocols

RUN git clone https://github.com/Hjdskes/cage.git cage && \
    cd cage && \
    git checkout v0.1.4

RUN cd /cage && \
    meson build && \
    ninja -C build

RUN /cage/build/cage --version
