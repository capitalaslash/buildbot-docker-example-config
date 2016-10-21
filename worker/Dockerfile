# buildbot/buildbot-worker-test

FROM        buildbot/buildbot-worker:master
MAINTAINER  Antonio Cervone <ant.cervone@gmail.com>

# This will make apt-get install without question
ARG         DEBIAN_FRONTEND=noninteractive

user root
# Install required npm packages
RUN  apt-get update && apt-get install -y -o APT::Install-Recommends=false -o APT::Install-Suggests=false \
        git \
        cmake \
        libeigen3-dev && \
    rm -rf /var/lib/apt/lists/*

user buildbot
