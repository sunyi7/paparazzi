FROM paparazziuav/pprz-dep
LABEL maintainer="felix.ruess@gmail.com"

RUN sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-stable.list'
RUN wget http://packages.osrfoundation.org/gazebo.key -O - | apt-key add -

RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get install -y \
    libgazebo7-dev \
    rustc cargo \
    && rm -rf /var/lib/apt/lists/*
