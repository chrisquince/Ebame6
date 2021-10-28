# Ebame6

# STRONG - Strain Resolution ON Graphs

## Overview

STRONG resolves strains on assembly graphs by resolving variants on core COGs using co-occurrence across multiple samples.

In this tutorial we will run the complete STRONG pipeline on a small AD time series. To 
begin we need to set-up our config file. This has been **mostly** prepared for you but will require a small amount of editing. 

## Getting started

Create a VM - EBAME-Quince preferably 8 cores xlarge

Then we activate the STRONG conda

```
conda activate STRONG
```

## Coassembly

Start off by moving into the /mnt directory create new directory Projects (if not already there) and subdirectory STRONG_AD:

```
cd ~/mydatalocal

mkdir Projects

cd Projects

mkdir STRONG_AD

cd STRONG_AD

```

Then copy in the short reads:

```

wget https://ebame6.s3.climb.ac.uk/data_small.tar.gz

cp /some/path/Tutorial/data_small.tar.gz .

tar -xvzf data_small.tar.gz


```
Have a look at the data folder structure:

```
ls data
```

Now copy in the STRONG config file:

```
cp ~/repos/Ebame21-Quince/configs/config.yaml .
```

We will begin by performing the SPADEs coassembly. First good practice it to check what would be run if command issued:

```
STRONG --config config.yaml Results assembly --threads 8 --dryrun --verbose
```

Then run coassembly for real:

```
STRONG --config config.yaml Results assembly --threads 8 --dryrun --verbose
```




