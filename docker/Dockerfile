FROM nagadomi/torch7:cuda10.1-cudnn7-devel-ubuntu18.04
RUN rm /etc/apt/sources.list.d/*

RUN apt-get update

RUN echo 'root:root' | chpasswd
RUN apt-get install -y openssh-server 
RUN sed -i 's/\#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -i 's/\#PermitEmptyPasswords no/PermitEmptyPasswords yes/' /etc/ssh/sshd_config

# clone main scripts
RUN git clone https://github.com/HiroIshida/siggraph2017_inpainting.git

