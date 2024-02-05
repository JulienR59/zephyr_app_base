FROM ghcr.io/zephyrproject-rtos/zephyr-build:latest

RUN sudo apt update && sudo apt install usbutils 

RUN cd /workdir && west init && west update && cd zephyr && source zephyr-env.sh