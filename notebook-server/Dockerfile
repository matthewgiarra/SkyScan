FROM python:3.9

RUN apt-get update
COPY pip.conf /etc/pip.conf
RUN pip3 install --upgrade pip
RUN pip3 install jupyter paho-mqtt
RUN mkdir /opt/notebooks
COPY ./Config.ipynb /opt/notebooks

ENTRYPOINT jupyter notebook --notebook-dir=/opt/notebooks --ip='*' --port=8888 --no-browser --allow-root --NotebookApp.token='' --NotebookApp.password=''
