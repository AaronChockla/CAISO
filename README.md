# CAISO

## Project Motivation
California leads the nation in adoption of renewable forms of power generation.  In so doing, there is growing concern over the stability of the power grid, as the primary sources of renewable power--wind and solar--are intermittent (*i.e.*, the sun doesn't always shine and the wind doesn't always blow), which disrupts the traditional steady state operation of the grid.  One way of mitigating this issue is through the use of energy storage.  This raises several questions regarding how much storage will be needed to ensure safe and reliable grid operation, as well as when those resources will need to be deployed.  To address these questions, data were pulled from the California Independent System Operator (*CAISO* oversees the operation of California's bulk electric power system, transmission lines, and electricity market generated and transmitted by its member utilities): http://oasis.caiso.com/mrioasis/logon.do

## Key Questions Addressed
* Assuming that the only sources of renewable power generation are wind and solar, what is the optimal mix to minimize the amount of storae needed, assuming that 100% of all power procured in the state comes from renewable energy resources?
* How much energy storage is going to be needed in California in a scenario where 100% of all power procured in the state comes from renewable energy resources?
* How long must energy be stored and how does this amount vary based on penetration of renewable generation resources on the grid (assuming the optimal mix of wind and solar is used)?
* By when will these storage assets need to be deployed to the grid in California?

## Project Files
* **\*.Demand csv files** contain power demand data in the CAISO system for each month from July 2018 through June 2019.
* **\*.Renewables csv files** contain power generation from renewable energy resources (wind and solar) in the CAISO system for each month from July 2018 through June 2019.
* **Results.csv** contains a cleaned dataset from processing the \*.Demand.csv and \*.Renewables.csv files and determining how much energy needs to be shifted and for how long.
* **CAISO.ipynb** python notebook for processing and analyzing CAISO data.
* **CAISO data.html** contains an html version of the python notebook.

## Libraries Used
**numpy** and **pandas** for data primary analysis

**os**, **datetime**, **time**, **pytz**, and **functools** for support data analyiss

**matplotlib** for data visualization

## Summary of Analysis
**1.** The optimal mix of renewables is ~30% solar and 70% wind in the scenario when 100% of demand must come from renewables.
**1.** Storage won't really be needed until renewable penetration reaches ~35%; for the 100% renewable scenario, about 50 terawatt hours (TWh) of energy will need to be shifted.
**1.** The duration of energy storage is tied to the amount of renewable generation - the more generation required to come from renewables sources, the longer energy needs to be stored.
**1.** A mix of storage duration assets will be needed between now and 2030, but most of the required storage capacity won't be needed until between 2030 and 2045.

## Acknowledgement
* CAISO for making these data publicly available along
* Various addtional resources cited in the ipynb file
