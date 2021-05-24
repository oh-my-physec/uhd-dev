# syntax=docker/dockerfile:1
FROM         ubuntu:20.04
MAINTAINER   Xing GUO

USER         root

RUN          apt-get update
RUN          apt-get install -y \
                 apt-transport-https software-properties-common
RUN          apt-get update

## GTK components
RUN          apt-get install -y \
                 python3-gi gobject-introspection gir1.2-gtk-3.0

RUN          apt-get install -y \
                 libuhd-dev libuhd3.15.0 uhd-host gnuradio

RUN          uhd_images_downloader

WORKDIR      /
