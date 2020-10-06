# fspm2020


## Demo requirements if you want to run it locally

`git clone https://github.com/fredboudon/fspm2020.git`

### Install with pip - inside conda env

Prepare conda environment: https://docs.conda.io/en/latest/miniconda.html

```bash
conda create -y -n pgl -c fredboudon -c conda-forge python=3.7 \
    openalea.lpy jupyterlab ipywidgets ipython=7 matplotlib rpy2 toml nodejs
```

Install and activate jupyter extension

```bash
conda activate pgl
pip install pgljupyter
jupyter labextension install --no-build @jupyter-widgets/jupyterlab-manager
jupyter lab build && jupyter lab
```

### Docker

```
docker pull jvail/plantgl-jupyter:0.1.21
docker run --rm \
    -p 8888:8888 \
    -v $PWD/examples:/home/jovyan/work jvail/plantgl-jupyter:0.1.21 \
    jupyter lab
```

## Introduction - Fred

* What are notebooks? A web based environment for scientists: https://jupytercon.com
* The Jupyter environment (notebooks, lab, hub)
* Integrating FSPM
* Question of Interactivity
* Parameter edition
* General Interests
* Pedagogical environment for academics
* Reproducible env

### Examples

* Integration [@nbviewer](https://nbviewer.jupyter.org/github/fredboudon/fspm2020/blob/master/examples/Integration.ipynb)

* RPy [@nbviewer](https://nbviewer.jupyter.org/github/fredboudon/fspm2020/blob/master/examples/RPy.ipynb)

* Parameter Edition [@nbviewer](https://nbviewer.jupyter.org/github/fredboudon/fspm2020/blob/master/examples/parameters/ParameterEdition.ipynb)


## Walkthrough plantgl-jupyter - Jan
* where do I find the project?
* what types of widgets are there?
* what is the api, options?
* ecosystem: binder, nbviewer
* where can I create feature requests, report bugs? - browse repository documentation?

## Application on a complex examples - Fred

* The vmango model

## Reproducibility and computational illustration - Christophe

* The hydroshoot model
