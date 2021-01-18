# Master_Dissertation
Scripts used to WRF-Chem processing, statistical script, post-processing to obtain results for current (Sep-Oct, 2018) and future (RCP 4.5 and RCP 8.5, Sep-Oct, 2030).

## VOC fraction
Two files `voc_frac.py` and  `htap2AE_year.py` developed by Gavidia (https://github.com/quishqa) were used to create VOC species emission files as input to WRF-Chem.

## LAPAt preprocessor emission model
LAPAt preprocessor emission model contents a namelist `namelist_fc.emi` and a NCL script `wrfchemi_cbmz_fc.ncl` developed by researchers of IAG as a utility for generating ready emission files for WRF-Chem.
`wrfchemi_cbmz_fc.ncl` was used in [Andrade et al. (2015)](https://www.frontiersin.org/articles/10.3389/fenvs.2015.00009/full). Please, cite this reference in case you want to use the `wrfchemi_cbmz_fc.ncl`.
Other files (grid03km_d02.txt, voc_split_cbmz.txt, wrfinput_d01) are needed to run `wrfchemi_cbmz_fc.ncl`.
