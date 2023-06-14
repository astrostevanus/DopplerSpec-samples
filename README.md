# DopplerSpec-samples
Examples of Doppler spectroscopy analysis using publicly available data.

Common dependencies:
PyAstronomy tqdm satrapy de423 jplephem h5py astroquery batman-package barycorrpy

Usually I install everything using pip and conda (since I use Anaconda):

pip install PyAstronomy tqdm satrapy de423 jplephem h5py astroquery batman-package barycorrpy

It would be helpful if you also install notebook extension which allow you to have collapsible headings, table of content, execute time, codefolding, etc.:

conda install -c conda-forge jupyter_contrib_nbextensions  widgetsnbextension 

Activate it using:
jupyter nbextensions_configurator enable --user
jupyter nbextension enable --py widgetsnbextension

The Jupyter notebook that I provide will guide you step-by-step from putting 1D spectrum to 2D array, putting the spectra into a common continuum profile, removing telluric/stellar lines using SysRem (detrending algorithm, Tamuz et al. 2014), cross-correlating with spectrum template, and summing all of the relevant signals (e.g. within in-transit phase in the case of transmission spectroscopy, or out of eclipse in the case of emission spectroscopy).


There are four available demo:
1. Near Infrared CARMENES data of HD 189733b which is publicly available through http://caha.sdc.cab.inta-csic.es/calto/. The data were used in Alonso-Floriano et al. 2018 (https://arxiv.org/abs/1811.08901 or https://www.aanda.org/articles/aa/pdf/2019/01/aa34339-18.pdf) to detect multiple water band detection in the atmosphere of HD 189733b.
2. HARPSN transmission spectroscopy of KELT-9b which was used for a publication in Hoeijmakers et al. 2018 (https://ui.adsabs.harvard.edu/abs/2018Natur.560..453H/abstract). The current version does not include on removing the Doppler shadow.
