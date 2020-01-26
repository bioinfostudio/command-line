FROM inducer/debian-amd64-minbase

RUN apt-get update --fix-missing
RUN apt-get -y -o APT::Install-Recommends=0 -o APT::Install-Suggests=0 install \
    curl \
    git \
    #python3-pip \
    #python3-setuptools \
    build-essential \
    nano \
    man \
    less

RUN apt-get clean
#RUN python3 -m pip install tornado terminado notebook
#RUN mkdir -p /opt/terminal
#ADD runterm /opt/terminal/

# create a non-root user
RUN useradd -ms /bin/bash bioinfo 

# copy the nice dotfiles that dockerfile/ubuntu gives us:
#RUN cd && cp -R .bashrc .profile /home/bioinfo
# setup the user directory
RUN chown -R bioinfo:bioinfo /home/bioinfo
RUN echo 'export PS1=" \W\$ "' >> /home/bioinfo/.bashrc
# become the bioinfo
USER bioinfo

ENV HOME /home/bioinfo
WORKDIR /home/bioinfo

# some example directories for the tutorial
RUN mkdir a_directory another_directory