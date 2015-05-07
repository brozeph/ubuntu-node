# Dockerfile for ubuntu-node
# Based on ubuntu

# Base image
FROM ubuntu:14.04

# Who to blame
MAINTAINER Joshua Thomas

# Download buid tools
RUN DEBIAN_FRONTEND=noninteractive \
	apt-get update && \
	apt-get dist-upgrade -y && \
	apt-get install build-essential git python -y && \
	sudo apt-get autoremove -y && \
	sudo apt-get autoclean -y

# Clone Node and build from source
RUN git clone https://github.com/joyent/node.git node
RUN cd node && git checkout v0.10.38 && ./configure && make && make install
