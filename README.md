# ansible-jupyter
uses the ansible kernel integration fo jupyter
https://github.com/ansible/ansible-jupyter-kernel#from-pypi
# install
```
pipenv install && \
pipenv run python -m ansible_kernel install --sys-prefix && \
pipenv run jupyter contrib nbextension install --sys-prefix && \
pipenv run jupyter nbextensions_configurator enable --sys-prefix && \
pipenv run jupyter-nbextension install rise --py --sys-prefix && \
echo JUPYTER_CONFIG_DIR=$(pipenv --venv)/etc/jupyter > .env
```
# run playbook
```
pipenv run jupyter notebook
```
open the notebook `ansible_demos.ipynb` 