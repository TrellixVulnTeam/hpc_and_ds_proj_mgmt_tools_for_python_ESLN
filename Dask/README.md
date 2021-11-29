# Dask tutorial

It also contains a modified version of the [Dask tutorial](https://github.com/dask/dask-tutorial) and summary notes
taken from [Dask documentation](https://docs.dask.org/en/stable/).

## Jupyter slides

All notebooks have been configured so that can be used for presenting them with "Jupyter slides". Use:

```
jupyter nbconvert <notebook_name>.ipynb --to slides --post serve
```

Jupyter `nbconvert` generates static html files useful for presentationsi. On the other hand, 
if you also want to execute the code during the presentation, 
install [RISE](https://rise.readthedocs.io/en/stable/):

```
pip install RISE
```

This library doesn't work **JupyterLab**, but for **Jupyter Notebooks**.


## Prerequisites
 
In order to be able to render Dask's **task graphs**, you must install [Graphviz](https://graphviz.org/download/) and and then its [python wrapper](https://pypi.org/project/graphviz/)

```
pip install graphviz
```


## Installation

Install Dask and all its dependencies:

```
pip install "dask[complete]"
```


## JupyterLab extensions

The following are JupyterLab extensions that allows to work better with Dask:

- [`dask-labextension`](https://github.com/dask/dask-labextension)

    - If you are using `jupyterlab>=3.0` just use:

    ```
    pip install jupyter_bokeh
    ```

    - If you are using `jupyterlab<3.0`, then first install:

    ```
    pip install dask_labextension
    ```

    and then build the client-side extension into JupyterLab with:

    ```
    jupyter labextension install dask-labextension
    ```

    - If you are using Jupyter Notebook 5.2 or earlier, then first install
    
    ```
    pip install dask_labextension
    ```

    and then enable the server extension by running

    ```
    jupyter serverextension enable --py --sys-prefix dask_labextension
    ```

## Tutorial's dependencies

Along with **Dask** and **Graphviz**, you must also install the next dependencies for running Dask's tutorial:

```
pip install numpy
pip install scipy
pip install pandas
pip install matplotlib
pip install h5py
pip install pillow
pip install toolz
pip install tables
pip install snakeviz
pip install scikit-image
```

Please note that `tables` corresponds to [PyTables](http://www.pytables.org/) package.

Be aware that not all the packages listed here are Dask dependencies, but they are needed for running
the notebooks in this tutorial.

You also need the next JupyLab extension:

- [`jupyter_bokeh`](https://github.com/bokeh/jupyter_bokeh)

    - For `jupyterlab>=3.0` use:

    ```
    pip install jupyter_bokeh
    ```

    - For `jupyterlab<3.0` use:

    ```
    jupyter labextension install @jupyter-widgets/jupyterlab-manager
    jupyter labextension install @bokeh/jupyter_bokeh
    ```
