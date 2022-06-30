# metisregimes
Calculate circulation regimes in the winter PacNA region, and characterize with atmospheric rivers

Calculate circulation regimes:

Data used: 
  twice-daily z500, u250 ERA5 PacNA NDJFM 1980-2019
  once daily z500, u250 Metis PacNA NDJFM 1986-2016

1. Low-pass filter the data using hpfilter_twice.ipynb

2. Remove the seasonal cycle and calculate anomalies using calcanoms_3_NDJFM_twice.ipynb

3. Perform PCA on the anomalies using calcPCs_4.ipynb

4. Calculate clusters from first 12 PCs

5. Identify how well regime composites are represented in ERA5 by Metis199, 639, 1279: Taylor_regimes.ipynb
    - This code depends on the taylorDiagram.py code
    - Acknowledgements: Y. Copin for this code

--------
Atmospheric rivers:

1. Get atmospheric river variables from ERA5: subset.AR.ERA5.ipynb

2. For ERA5 data: calculate moisture flux using calc_vqvi.AR.ERA5.ipynb

3. Identify atmospheric rivers given moisture flux using AR_notrack_2.ipynb

4. Calculate anomalies from the mean number of atmospheric rivers using AR_notrack_3.calcanoms.ipynb