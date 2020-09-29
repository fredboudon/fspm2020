FROM jvail/plantgl-jupyter:0.1.18

ARG NB_USER=jovyan
ARG NB_UID=1000

COPY . /home/${NB_USER}
USER root
RUN conda install -y -c conda-forge pandas matplotlib rpy2
RUN chown -R ${NB_UID} /home/${NB_USER}
WORKDIR /home/${NB_USER}

USER ${NB_USER}
