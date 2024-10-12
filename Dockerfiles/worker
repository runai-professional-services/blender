FROM nvidia/cudagl:11.3.0-devel-ubuntu20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt upgrade -y && apt install -y wget xz-utils libglu1-mesa libxi6 libxrender1 libsm6 libxext6 \
    libglu1-mesa libxxf86vm1 libxfixes3 libxkbcommon0 libgl1 libgl1-mesa-dri mesa-utils libglu1-mesa-dev python3 \
    python3-pip

RUN mkdir -p /etc/flamenco /etc/blender

RUN wget https://flamenco.blender.org/downloads/flamenco-3.5-linux-amd64.tar.gz -O /tmp/flamenco.tar.gz
RUN wget https://mirrors.ocf.berkeley.edu/blender/release/Blender4.2/blender-4.2.2-linux-x64.tar.xz -O /tmp/blender.tar.xz

RUN tar -xzf /tmp/flamenco.tar.gz -C /etc/flamenco --strip-components=1
RUN tar -xf /tmp/blender.tar.xz -C /etc/blender --strip-components=1


WORKDIR /etc/flamenco

EXPOSE 8080

CMD ["sleep", "infinity"]