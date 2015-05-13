# BrainPiglet HI
This repository contains model definitions and input data used for the extended piglet hypoxia-ischaemia model, BrainPigletHI.

## Models
The `models` directory contains model definitions in [BCMD][bcmd] format. The main model is in the file `bp20.modeldef`. By default this imports an additional file, `bp20_insult.modeldef`, which defines some additional variables to support testing of three possible explanatory scenarios for non-recovery after HI. These additions are not needed when running the model for recovering data. They should not cause any harm, but you can omit them by commenting out the import statement in the main file.

## Data
Experimental data from the two piglets LWP180 and LWP188 are included in the `csv` directory. The subdirectory `csv` provides the data in CSV format, while the `inputs` file contains only the input data for the model, in BCMD input format. Two additional input files, named with the suffix `_init`, specify the parameters defining the insult period for the `bp20_insult.modeldef` model addition. These are required when running optimisations that attempt to account for the different scenarios. They are not needed in other cases -- the default parameterisation should suffice.

[bcmd]: https://github.com/bcmd/BCMD