FROM ubuntu:20.04
LABEL maintainer "Samuel Jacobs <samjacobs@scimulate.com>"

RUN apt-get update && apt-get install -y wget
WORKDIR /tmp
RUN wget https://files.salome-platform.org/Salome/Salome9.9.0/SALOME-9.9.0.tar.gz
RUN tar xzvf SALOME-9.9.0.tar.gz

RUN apt-get update && DEBIAN_FRONTEND=noninteractive TZ="America/New York" apt-get install -y \
    python3 \
    libglu1 \
    wget \
    libopengl0 \
    libfontconfig1 \
    libsm6 \
    dbus-x11 \
    libglib2.0-dev \
    libpangoft2-1.0-0 \
    libpangocairo-1.0-0 \
    libgdk-pixbuf2.0-0 \
    libpango1.0-dev \
    libvtk6.3 \
    libvtk6.3-qt \
    libegl1 \
    xterm \
    netcat

CMD /tmp/SALOME-9.9.0/mesa_salome 

#COPY SALOME-9.9.0.tar.gz /tmp
#WORKDIR /tmp
#RUN tar xzvf SALOME-9.9.0.tar.gz

#RUN apt-get update && DEBIAN_FRONTEND=noninteractive TZ="America/New York" apt-get install -y \
#    python3 \
#    libglu1 \
#    wget \
#    libopengl0 \
#    libfontconfig1 \
#    libsm6 \
#    dbus-x11 \
#    libglib2.0-dev \
#    libpangoft2-1.0-0 \
#    libpangocairo-1.0-0 \
#    libgdk-pixbuf2.0-0 \
#    libpango1.0-dev \
#    libegl1 \
#    xterm \
#    netcat \

#CMD /tmp/SALOME-9.9.0/mesa_salome 
