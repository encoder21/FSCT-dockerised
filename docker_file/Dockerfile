# FROM nvidia/cuda:12.5.0-base-ubuntu20.04
FROM nvidia/cuda:11.1.1-base-ubuntu20.04

# export timezone for python3.9
ENV TZ=Europe/Rome
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update
RUN apt-get install -y apt-utils
RUN apt-get install -y curl
RUN apt-get install -y git
RUN apt-get install -y nano
RUN apt-get install -y python3.9
RUN apt-get install -y python3.9-distutils
RUN curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
RUN python3.9 get-pip.py --user
RUN git clone https://github.com/encoder21/FSCT.git /app/FSCT
WORKDIR /app/FSCT
RUN python3.9 -m pip install -r requirements.txt
CMD python3.9 scripts/train.py
# CMD tail -f /dev/null
