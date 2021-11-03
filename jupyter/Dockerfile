FROM jupyter/scipy-notebook:latest
# COPY ./requirements.txt /tmp/
# RUN pip install --requirement /tmp/requirements.txt
USER root
RUN pip install cassandra-driver
# CMD start-notebook.sh