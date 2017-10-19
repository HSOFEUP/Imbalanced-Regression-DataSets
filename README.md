# Data sets for Imbalanced Regression Learning
## 15 data sets for imbalanced regression from different domains


## Contents

This repository contains the 15 data sets used in the paper:

Paula Branco, Luis Torgo, and Rita P. Ribeiro <strong>"Pre-processing Approaches for Imbalanced Distributions in Regression"</strong> submitted to Neurocomputing Journal.

The data sets are available in 3 formats: Rdata, csv and arff.

You can either download the data sets in all formats, or in one desired format.

This [page](https://paobranco.github.io/Imbalanced-Regression-DataSets/) allows you to select and download the data format.

## More details on the data sets

The main characteristics of the 15 regression data sets in this folder are as follows:

ID   | Data Set   | N    | tpred | p.nom | p.num | nRare | % Rare |
-----|------------|------|-------|-------|-------|-------|--------|
DS1  | a6         | 198  | 11    | 3     | 8     | 33    | 16 7   |
DS2  | Abalone    | 4177 | 8     | 1     | 7     | 679   | 16.3   |
DS3  | a3         | 198  | 11    | 3     | 8     | 32    | 16.2   |
DS4  | a4         | 198  | 11    | 3     | 8     | 31    | 15.7   | 
DS5  | a1         | 198  | 11    | 3     | 8     | 28    | 14.1   |
DS6  | a7         | 198  | 11    | 3     | 8     | 27    | 13.6   |
DS7  | boston     | 506  | 13    | 0     | 13    | 65    | 12.8   |
DS8  | a2         | 198  | 11    | 3     | 8     | 22    | 11.1   |
DS9  | fuelCons   | 1764 | 38    | 12    | 26    | 164   | 9.3    |
DS10 | heat       | 7400 | 13    | 4     | 9     | 664   | 9.0    |
DS11 | availPwr   | 1802 | 16    | 7     | 9     | 157   | 8.7    |
DS12 | cpuSm      | 8192 | 13    | 0     | 13    | 713   | 8.7    |
DS13 | maxTorque  | 1802 | 33    | 13    | 20    | 129   | 7.2    |
DS14 | bank8FM    | 4499 | 9     | 0     | 9     | 288   | 6.4    |
DS15 | Accel      | 1732 | 15    | 3     | 12    | 89    | 5.1    |

where,

N represents the total number of cases;

tpred represents the number of predictors;

p.nom represents the number of nominal predictors;

p.num represents the number of numeric predictors;

nRare represents the number of cases with target variable relevance above 0.8; and

% Rare=nRare/N.


## Directly importing the data sets into R

To import the .Rdata file directly into **R** you will need the `repmis` and `DMwR` R packages.

You can install them as follows:

```r
install.packages(c("repmis", "DMwR"))
```



Then, load the libraries:

```r
library(DMwR)
library(repmis)
```

And use the `source_data` function:

```r
repmis::source_data(url = "https://github.com/paobranco/Imbalanced-Regression-DataSets/blob/master/RDATA_data/DataSets15.Rdata?raw=true")
```

This will load into R an object named `DSs` which contains a list with 15 objects of class `dataset` from package DMwR.


You can acces and explore the data sets as follows.

Observe the first task:


```r
DSs[[1]]
```

In particular for this data set, you may check it's name and the formula of the task.


```r
DSs[[1]]@name
DSs[[1]]@formula
```

See the first lines of the first data set:

```r
head(DSs[[1]]@data)
```

