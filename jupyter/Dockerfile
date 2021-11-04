FROM jupyter/scipy-notebook:2021-11-01
USER root
COPY ./1000-steam-user-library.json "/home/${NB_USER}/work"
COPY ./json_einlesen.ipynb "/home/${NB_USER}/work"
COPY ./basic_cassandra_demo.ipynb "/home/${NB_USER}/work"
RUN pip install cassandra-driver==3.25.0
