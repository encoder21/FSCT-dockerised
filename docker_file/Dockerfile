FROM nvidia/cuda:11.1.1-base-ubuntu20.04

# export timezone for python3.9
ENV TZ=Europe/Rome
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get update
RUN apt-get install -y apt-utils
RUN apt-get install -y nano
RUN apt-get install -y git
RUN apt-get install -y python3.9
RUN apt-get install -y pip
RUN git clone https://github.com/encoder21/FSCT.git /app/FSCT
WORKDIR /app/FSCT
RUN pip install -r requirements.txt
CMD python scripts/train.py
# CMD tail -f /dev/null
