# Master_Dissertation
Scripts used to WRF-Chem processing, statistical script, post-processing to obtain results for current (Sep-Oct, 2018) and future (RCP 4.5 and RCP 8.5, Sep-Oct, 2030).

## VOC fraction
Two files `voc_frac.py` and  `htap2AE_year.py` developed by Gavidia (https://github.com/quishqa) were used to create VOC species emission files as input to WRF-Chem.

## LAPAt preprocessor emission model
LAPAt preprocessor emission model contents a namelist `namelist_fc.emi` and a NCL script `wrfchemi_cbmz_fc.ncl` developed by researchers of IAG as a utility for generating ready emission files for WRF-Chem.
`wrfchemi_cbmz_fc.ncl` was used in [Andrade et al. (2015)](https://www.frontiersin.org/articles/10.3389/fenvs.2015.00009/full). Please, cite this reference in case you want to use the `wrfchemi_cbmz_fc.ncl`.
Other files (grid03km_d02.txt, voc_split_cbmz.txt, wrfinput_d01) are needed to run `wrfchemi_cbmz_fc.ncl`.

### Total number and type of vehicles based on each modeling domain area
`DATA_EF.xlsx`contents information collected from CETESB emission reports and DENATRAN that it is reading in the jupyter notebook `Fleet and Use intensity September 2018.ipynb` and `Fleet and Use intensity October 2018.ipynb`.
These jupyter notebooks content scripts that let us approximate total number of vehicles and proportion by type and fuel consumption.

## Emission analyses
Two jupyter notebook called `Emissions_wrfchemi Exp10.ipynb` and `Emissions_wrfchemi Exp10 October 2018.ipynb` content scripts in Python 3 to analize emissions ready by WRF-Chem and generate Charts used for the Master Dissertation.

## WRF-Chem model results processing
WRF-Chem model outputs are files format (`wrfout_<domain>_{year}-{m}-{d}_{h}:00:0`) that content matrix values for many parameters meteorological and chemical species.

There are scripts and Jupyter Notebooks used to process WRF-Chem outputs:

* `wrf_extract.py`: Script developed by M. Gavidia [quishqa](https://github.com/quishqa). This script extract meteorological and polutants variables such as temperature (t2), relative humidity (rh2), wind, atmospheric pressure (psfc), ozone (o3), nitrogen monoxide (no), nitrogen dioxide (no2), and carbon monoxide (co). This script requires location points as latitude and longitude. In this case, we used CETESB locations provided in its website (QUALAR). Pollutants (with the exception of carbon monoxide) were converted from ppm to $\mu$gm$^{-3}$. After that, variables extracted were saving as dictionary and exporting to csv format.
* `wrf_rain.py`: Script based on `wrf_extract.py` that extracts `rain` and `rainnc`. These variables are accumulated rain and require to be processed. Finally, the script export values based on location as dictionary saving as pickle (very useful in Python).
* `mod_stats.py`: Script developed by M. Gavidia [quishqa](https://github.com/quishqa) and modified by me. This script analyze model outputs and observed values and calculate values for each statistical benchmarks.
* Jupyter Notebooks: `3.1 Evaluation of simulation Results for September 2018.ipynb` for instance contents Python scripts used to obtain charts and statistical results. `3.2 Meteorological results evaluation` also is similar to before one, but it process meteorological outputs.

## ACKNOWLEDGMENTS
The author thank the CAPES (Coordenação de Aperfeiçonamento de Pessoal de Nível Superior) for the financial support of this work. I also thank the State Company for the Environment (CETESB) for the hourly data from the station networks available as open acces in its website (QUALAR).
