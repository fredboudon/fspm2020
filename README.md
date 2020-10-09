# FSPM 2020 Demo session on virtual modelling environments


## Demo requirements if you want to run it locally


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

## Program

### Introduction - Fred

* What are notebooks? A web based environment for scientists: https://jupytercon.com
* The Jupyter environment (notebooks, lab, hub) and ecosystem
* Pedagogical environment for academics
* Reproducible env
* Integrating FSPM
* Question of Interactivity
* Parameter edition
* General Interests

[![Jupyter](https://jupyter.org/assets/nav_logo.svg)](https://jupyter.org/)

#### Examples [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fredboudon/fspm2020.git/master?filepath=examples)


* Integration [![NBViewer](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/fredboudon/fspm2020/blob/master/examples/Integration.ipynb) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fredboudon/fspm2020.git/master?filepath=examples%2FIntegration.ipynb)

* RPy [![NBViewer](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/fredboudon/fspm2020/blob/master/examples/RPy.ipynb) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fredboudon/fspm2020.git/master?filepath=examples%2FRPy.ipynb)

* Parameter Edition [![NBViewer](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/fredboudon/fspm2020/blob/master/examples/parameters/ParameterEdition.ipynb) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fredboudon/fspm2020.git/master?filepath=examples%2Fparameters%2FParameterEdition.ipynb)

If you run the demo locally, you should type in your conda shell
```
git clone https://github.com/fredboudon/fspm2020.git
cd fspm2020/examples
jupyter notebook .
```
You can select the different ipynb files of the demo.

### Walkthrough plantgl-jupyter - Jan

* where do I find the project: https://github.com/jvail/plantgl-jupyter
* features, widgets
* api, options
* ecosystem: binder, nbviewer, cloud (e.g. ifb biosphere), vscode
* documentation, request features, report bugs

#### Examples

To run the demo locally
```
git clone https://github.com/jvail/plantgl-jupyter.git
cd examples
jupyter lab .
```


### Application on a complex example - Fred

* The vmango model : https://github.com/fredboudon/vmango/tree/fspm2020
* Mix of stochastic architectural development with mecanistic fruit growth models

#### Examples
* vmango  [![NBViewer](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/fredboudon/vmango/blob/fspm2020/notebooks/vmango.ipynb)
* vmango ochard  [![NBViewer](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/fredboudon/vmango/blob/fspm2020/notebooks/vmango_2.ipynb)

Binder version (slow) : [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fredboudon/vmango.git/fspm2020?urlpath=lab/tree/notebooks)	

To run the demo locally
```
git clone https://github.com/fredboudon/vmango.git
git checkout fspm2020
python setup.py install
cd notebooks
jupyter lab .
```


### Gallery of OpenAlea notebooks from published articles - Christophe

* The OpenAlea Read The Docs website : https://openalea.readthedocs.io/en/latest/tutorials/index.html
* The hydroshoot model  [![NBViewer](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/openalea/openalea.rtfd.io/blob/master/example/hydroshoot_grapevine.ipynb)
