# our base image
FROM ubuntu:xenial

RUN mkdir /home/dst
WORKDIR /home/dst

COPY requirements.txt requirements.txt

RUN apt update
RUN apt install python3-pip -y
RUN pip3 install -r requirements.txt
RUN rm -rf requirements.txt

# RUN pip3 install jupyterlab

CMD ["jupyter-notebook", "--ip=0.0.0.0", "--allow-root", "--NotebookApp.token=''", "--no-browser"]
