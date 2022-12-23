# Commonly used commands
## jupyter notebook / jupyter lab
### Adding conda venv to ipython kernels
```bash
ipython kernel install --user --name=VENV_NAME
```
### Error displaying widget
1. make sure node.js and npm are properly installed
2. reinstall ipywidgets
```
pip install ipywidgets
conda install -c conda-forge ipympl
```
or try reinstall jupyter-matplotlib
```
jupyter labextension install js
```
or try reinstall everything
```
jupyter labextension uninstall jupyter-matplotlib && jupyter labextension uninstall @jupyter-widgets/jupyterlab-manager && conda update -y widgetsnbextension && conda update -y nodejs && pip uninstall -y ipympl && pip install git+https://github.com/matplotlib/jupyter-matplotlib.git#egg=ipympl && conda update jupyterlab -y && jupyter labextension install @jupyter-widgets/jupyterlab-manager && jupyter labextension install jupyter-matplotlib && jupyter labextension update --all && jupyter lab build && jupyter nbextension list && jupyter labextension list
```
