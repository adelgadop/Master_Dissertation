# Master_Dissertation
Utilities used for Anthropogenic emissions calculation.

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

## ACKNOWLEDGMENTS
The author thank the CAPES (Coordenação de Aperfeiçonamento de Pessoal de Nível Superior) for the financial support of this work. I also thank the State Company for the Environment (CETESB) for the hourly data from the station networks available as open acces in its website (QUALAR).
