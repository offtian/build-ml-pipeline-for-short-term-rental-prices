FROM continuumio/miniconda3:4.10.3p1

WORKDIR /project

RUN conda install \
    numpy \
    pandas \
    matplotlib \
    jupyterlab \ 
    seaborn \
    pandas-profiling \
    pyarrow

RUN pip install wandb mlflow

COPY ./MLproject /project
COPY ./EDA.ipynb /project

CMD ["jupyter-lab","--ip=0.0.0.0","--no-browser","--allow-root"]
