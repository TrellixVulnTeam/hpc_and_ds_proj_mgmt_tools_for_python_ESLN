# Dask tutorial

Repository intended to document exploration about Dask and its capabilities

## Installation

Follow the next steps:

1. In order to be able to render Dask's **task graphs**, you must install [Graphviz](https://graphviz.org/download/) and and then its [python wrapper](https://pypi.org/project/graphviz/)

```
pip install graphviz
```

2. Install Dask

```
pip install "dask[complete]"
```

## JupyterLab extensions

Install JupyterLab extensions:

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
## Jupyter slides

All notebooks have been configured so that can be used for presenting them with Jupyter slides. Use:

```
jupyter nbconvert <notebook_name>.ipynb --to slides --post serve
```

Jupyter slised generates static html files useful for presentations. On the other hand, if you also want to execute the code during the presentation, install [RISE](https://rise.readthedocs.io/en/stable/):

```
pip install RISE
```

This library doesn't work **JupyterLab**, but for **Jupyter Notebooks**.




## Other

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

# TODO

- Include a chapter on profiling
- Include a chapter on parallelism and parallelization strategies