<h1>
hvPlot <img src="/doc/_static/logo.png" width="50" height="50">
</h1>

**A high-level plotting API for the PyData ecosystem built on HoloViews.**

|    |    |
| --- | --- |
| Build Status | [![Build Status](https://github.com/holoviz/hvplot/workflows/tests/badge.svg?query=branch%3Amaster)](https://github.com/holoviz/hvplot/actions?query=workflow%3Atests+branch%3Amaster) |
| Coverage | [![Coverage Status](https://coveralls.io/repos/github/holoviz/hvplot/badge.svg?branch=master)](https://coveralls.io/github/holoviz/hvplot?branch=master) |
| Latest dev release | [![Github tag](https://img.shields.io/github/tag/holoviz/hvplot.svg?label=tag&colorB=11ccbb)](https://github.com/holoviz/hvplot/tags) |
| Latest release | [![Github release](https://img.shields.io/github/release/holoviz/hvplot.svg?label=tag&colorB=11ccbb)](https://github.com/holoviz/hvplot/releases) [![PyPI version](https://img.shields.io/pypi/v/hvplot.svg?colorB=cc77dd)](https://pypi.python.org/pypi/hvplot) [![hvplot version](https://img.shields.io/conda/v/pyviz/hvplot.svg?colorB=4488ff&style=flat)](https://anaconda.org/pyviz/hvplot) [![conda-forge version](https://img.shields.io/conda/v/conda-forge/hvplot.svg?label=conda%7Cconda-forge&colorB=4488ff)](https://anaconda.org/conda-forge/hvplot) [![defaults version](https://img.shields.io/conda/v/anaconda/hvplot.svg?label=conda%7Cdefaults&style=flat&colorB=4488ff)](https://anaconda.org/anaconda/hvplot) |
| Docs | [![gh-pages](https://img.shields.io/github/last-commit/holoviz/hvplot/gh-pages.svg)](https://github.com/holoviz/hvplot/tree/gh-pages) [![site](https://img.shields.io/website-up-down-green-red/http/hvplot.holoviz.org.svg)](http://hvplot.holoviz.org) |


## What is it?

The PyData ecosystem has a number of core Python data containers that allow users to work with a wide array of datatypes, including:

* [Pandas](http://pandas.pydata.org): DataFrame, Series (columnar/tabular data)
* [XArray](http://xarray.pydata.org): Dataset, DataArray (multidimensional arrays)
* [Dask](http://dask.pydata.org): DataFrame, Series, Array (distributed/out of core arrays and columnar data)
* [Streamz](http://streamz.readthedocs.io): DataFrame(s), Series(s) (streaming columnar data)
* [Intake](http://github.com/ContinuumIO/intake): DataSource (data catalogues)
* [GeoPandas](http://geopandas.org): GeoDataFrame (geometry data)
* [NetworkX](https://networkx.github.io/documentation/stable/): Graph (network graphs)

Several of these libraries have the concept of a high-level plotting API that lets a user generate common plot types very easily. The native plotting APIs are generally built on [Matplotlib](http://matplotlib.org), which provides a solid foundation, but means that users miss out the benefits of modern, interactive plotting libraries for the web like [Bokeh](http://bokeh.org) and [HoloViews](http://holoviews.org).

hvPlot provides a high-level plotting API built on HoloViews that provides a general and consistent API for plotting data in all the abovementioned formats. hvPlot can integrate neatly with the individual libraries if an extension mechanism for the native plot APIs is offered, or it can be used as a standalone component.

To start using hvplot have a look at the [Getting Started Guide](https://hvplot.holoviz.org/getting_started/index.html) and check out the current functionality in the [User Guide.](https://hvplot.holoviz.org/user_guide/index.html)

<img src="http://blog.holoviz.org/images/hvplot_collage.png">

## Installation

hvPlot supports Python 2.7, 3.5, 3.6 and 3.7 on Linux, Windows, or Mac and can be installed with ``conda``:

```
conda install -c pyviz hvplot
```

or with ``pip``:

```
pip install hvplot
```

In the classic Jupyter notebook environment and JupyterLab objects returned by hvPlot will then render themselves if they are the last item in a notebook cell. For versions of `jupyterlab>=3.0` the necessary extension is automatically bundled in the `pyviz_comms` package, which must be >=2.0. However note that for version of `jupyterlab<3.0` you must also manually install the JupyterLab extension with:

```bash
jupyter labextension install @pyviz/jupyterlab_pyviz
```

