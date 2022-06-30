# metisregimes
Calculate circulation regimes in the winter PacNA region, and characterize with atmospheric rivers

Data used: 
  twice-daily z500, u250 ERA5 PacNA NDJFM 1980-2019
  once daily z500, u250 Metis PacNA NDJFM 1986-2016

1. Low-pass filter the data using hpfilter_twice.ipynb

2. Remove the seasonal cycle and calculate anomalies using
