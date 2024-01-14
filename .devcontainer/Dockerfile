FROM ghcr.io/zephyrproject-rtos/zephyr-build:latest

RUN west init /workdir/zephyrproject
RUN cd /workdir/zephyrproject
RUN ls -l
RUN pwd
RUN west update /workdir/zephyrproject

RUN zephyr-export



