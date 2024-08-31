FROM ghcr.io/zephyrproject-rtos/zephyr-build:latest


# Install necessary tools
RUN sudo apt update && sudo apt upgrade -y

# Installing cross-compilation toolchain 
RUN wget --no-check-certificate -O - https://developer.arm.com/-/media/Files/downloads/gnu-rm/10-2020q4/gcc-arm-none-eabi-10-2020-q4-major-x86_64-linux.tar.bz2 | tar xjf -

# NRF command line tools are installed, because they come with a JLink DEB package
RUN wget --no-check-certificate https://nsscprodmedia.blob.core.windows.net/prod/software-and-other-downloads/desktop-software/nrf-command-line-tools/sw/versions-10-x-x/10-23-0/nrf-command-line-tools_10.23.0_amd64.deb
RUN sudo apt install -y ./nrf-command-line-tools_10.23.0_amd64.deb

RUN sudo apt install udev -y
RUN sudo /lib/systemd/systemd-udevd --daemon && sudo apt install -y /opt/nrf-command-line-tools/share/JLink_Linux_V788j_x86_64.deb --fix-broken