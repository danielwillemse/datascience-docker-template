FROM quay.io/jupyter/pytorch-notebook

COPY --chown=${NB_UID}:${NB_GID} requirements.txt /tmp/
RUN pip install -r /tmp/requirements.txt

RUN fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"
 
# ENV JUPYTER_ENABLE_LAB=yes