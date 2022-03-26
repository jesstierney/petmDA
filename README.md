# petmDA
This is a public repository containing data and results for the Paleocene-Eocene Thermal Maximum data assimilation (PETM-DA), which is described in the submitted paper:

Tierney, J. E., Zhu, J., Li, M., Ridgwell, A., Hakim, G. J., Poulsen, C. J., Whiteford, R. D. M., Rae, J. W. B., and Kump, L. Spatial patterns of climate change across the Paleocene-Eocene Thermal Maximum, submitted to Proceedings of the National Academy of Sciences, March 2022.

**Please be advised this paper has yet to be peer reviewed so all files here are preliminary**

## Guide to the files

### ProxyData

In this folder you will find: 

**petmTData.csv** The temperature proxy data used to constrain the PETM-DA. Data are given in proxy units as timeslice averages for the prePETM and PETM climate states, respectively. Metadata includes site name, modern coordinates, paleo coordinates on the [Herold 2014](https://doi.org/10.5194/gmd-7-2077-2014) reconstruction, estimated paleodepth, proxy type, cleaning method (for Mg/Ca), preservation (for foraminiferal proxies; 0 = glassy, 1 = frosty), genus (for foraminiferal proxies), data source and doi, and the assessment of how the PETM and prePETM boundaries were determined---mostly, these were drawn from [deepMIP](https://doi.org/10.5194/gmd-12-3149-2019). 

**validationData.xlsx** Compiled independent terrestrial temperature, hydroclimate, and leaf wax D/H data that were used to validate the PETM-DA. These data were not assimilated but rather are used as external checks on the validity of the results. The sheet "TerrestrialTemp" has quantitative temperature estimates from pollen, leaf-based methods, and clumped isotopes (D47) for the PETM and prePETM timeslices respectively. The sheet "PminusE" has qualitative estimates of hydroclimate change (1 = wetter, -1 = drier) based on changes in plants or pollen, dinocysts, or clay minerology (presence of palygorskite). The sheet "LeafWaxdD" has quantitative estmates of the change in the &delta;D of precipitation during the PETM (note however in some cases the standard error exceeds the mean change, hence indicating a non-significant shift).

### PosteriorResults

In this folder you will find:

**PETMDA_ATM_annual.nc** Mean annual posterior values for atmospheric variables, including surface temperature (tas), precipitation (pr), evaporation (evap), the isotopes of precipitation (d18op and dDp), and low cloud cover (lowcloud). All values have associated 1-sigma errors (variables that end with "std") from the ensemble DA results. These data are on a 1.9 (latitude) by 2.5 (longitude) rectangular grid. The timestep is 1 = PETM, 2 = prePETM.

**PETMDA_ATM_monthly_climo.nc** Monthly climatological values for atmospheric variabiles, including surface temperature (tas), precipitation (pr), evaporation (evap), and snow thickness (snow). All values have associated 1-sigma errors (variables that end with "std") from the ensemble DA results. These data are on a 1.9 (latitude) by 2.5 (longitude) rectangular grid. The timestep is 1 = PETM, 2 = prePETM.

**PETMDA_OCN_annual.nc** Mean annual posterior values for oceanic variables, including sea-surface temperature (sst), sea-surface salinity (sss), and the &delta;<sup>18</sup>O of surface seawater (d18osw). All values have associated 1-sigma errors (variables that end with "std") from the ensemble DA results. These data are on a nominal 1 degree Greenland pole grid. Specifically this is the POP ocean model gx1v6 tripolar grid.

**PETMDA_SST_monthly_climo.nc** Monthly climatological values for sea-surface temperature (sst). 1-sigma errors are provided as sst_std. These data are on a nominal 1 degree Greenland pole grid. Specifically this is the POP ocean model gx1v6 tripolar grid.
