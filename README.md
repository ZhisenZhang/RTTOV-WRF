# RTTOV-WRF
Simulate SEVIRI satellite channels from WRF output

- Input: wrfout file (NetCDF format) written by WRF
- Output: brightness temperatures or reflectances

### NetCDF output
with path to wrfout file as argument:

`python rttov_wrf.py somepath/wrfout_d01_2008-07-30_18:00:00 VIS`
creates `somepath/RTout_2008-07-30_18:00:00.nc` 

### xarray output 
    config = setup_IR()
    config = setup_VIS()
    dsout = call_pyrttov(ds, config)

### Install
1) download and compile RTTOV from [nwpsaf.eu](https://www.nwpsaf.eu/site/software/rttov/).
2) get the `pysolar` module
3) configure the python script `rttov_wrf.py`, it sets all the assumptions for radiative transfer.


### Note:
The python version calling `rttov_wrf.py` must be the same as the one used for compiling RTTOV.
