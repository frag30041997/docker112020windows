FROM ubuntu

WORKDIR /usr/src/workspace
COPY . .
RUN apt-get -y update

RUN apt-get -y install python3 \
&& apt-get -y install python3-pip \
&& apt-get install -y git \
&& apt-get install -y vim \
&& pip3 install -r requirements.txt \
&& git config --global user.name frag \
&& git config --global user.email fragfalse@gmail.com \
&& git clone https://github.com/frag30041997/docker112020windows.git

EXPOSE 8000
CMD ["jupyter", "notebook", "--port=8000", "--no-browser", "--ip=0.0.0.0", "--allow-root"]