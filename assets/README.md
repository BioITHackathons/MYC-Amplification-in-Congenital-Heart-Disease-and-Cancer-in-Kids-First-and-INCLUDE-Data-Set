# assets for input to the repository
#
Jupyter Lab has problems with install Tidyverse

To fix this reference this discovery.

[tidyverse not installed in notebook](https://community.rstudio.com/t/tidyverse-package-does-not-install/162507/3)

missing were systemfonts which need to be installed in the terminal window.

Just installing what the jupyterlab notebook said was missing.

```
sudo apt update
sudo apt upgrade
sudo apt-get install libcurl4-openssl-dev
sudo apt-get install libfontconfig1-dev
sudo apt-get install libharfbuzz-dev libfribidi-dev
sudo apt-get install libfreetype6-dev libpng-dev libtiff5-dev libjpeg-dev

```

Still had issues with `ragg`.

THis was solved by from a terminal window within the Jupyterlab notebook.

```
conda install -c conda-forge pkg-config
```



