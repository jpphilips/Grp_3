## Multi-Zonal Regression Analysis of Density Log Data

### Project Description
The goal of this project is to perform a multi-zonal regression analysis of density log data obtained from a location in the US Gulf of Mexico. The dataset (gmdata3.csv) contains measured depth (DEPTH) and density log values for different zones within a borehole. We aim to predict density using the Amoco correlation and visualize the results.

### Table of Contents
* Introduction 
* Data Overview
* Installation
* Usage
* Methodology
* Results
* Contributing
* License
* Authors

### Introduction

Density logs provide valuable information about subsurface lithology and fluid content. In this project, we analyze density log data from six different zones (A, B, C, D, E, F) and predict density using the Amoco correlation. Additionally, we calculate overburden stress profiles throughout the well.
### Data Overview
* Dataset: gmdata3.csv
* Columns: DEPTH & Density Log 
###### DEPTH: Measured depth (in feet)
###### Density Log: Density log values (in g/cm³)

### Installation
Clone this repository:
```bash
git clone https://github.com/jpphilips/Grp_3.git
cd /Grp_3
```
Install required Python libraries:
```
pip install pandas numpy matplotlib
```
Import needed libraries:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from scipy.optimize import curve_fit
from sklearn.experimental import enable_iterative_imputer
from sklearn.impute import IterativeImputer
```
### Usage
1. #### Load the data:
* Ensure gmdata3.csv is in the project directory.
```
cd .../Grp_3/.../gmdata3.csv
```
* Run the Python script to read the data into a Pandas DataFrame.
```
df = pd.read_csv('gmdata3.csv')
```
2. #### Data Preprocessing:
* Reindex the DataFrame by depth.
* Replace missing values with np.nan.
* Separate data into zones.
3. #### Amoco Correlation:
* Implement the Amoco correlation formula to predict density.
* Calculate parameters (α, β, γ) for each zone.
4. #### Overburden Stress:
* Use density and depth to calculate overburden stress.
5. #### Visualization:
* Create well log plots showing predicted density and available density data.
* Highlight different zones.

### Methodology
#### Amoco Correlation:
```
ρ = α + (D-w/3125) ^ γ
```
* ρ: Predicted density (g/cm³)
* D: True vertical depth (feet)
* w: Water depth (feet)

#### Overburden Stress:
Overburden stress = density × gravitational acceleration × depth 

### Results
* Display the well log plot with predicted density and available density data.
* Compare the predicted density with actual measurements.

### Contributing
* Contributions are welcome! Please open an issue or submit a pull request.
* Please make sure to update tests as appropriate.

### License
* [IPES](https://ipes.uniport.edu.ng/)
* [IFP](https://www.ifp-school.com/en/)
* [UNIPORT](https://www.uniport.edu.ng/index.php)

## Authors:
* [PHILIP JOSEPH OLUKA](https://github.com/jpphilips)
* [OKONKWO MATTHEW O.](https://github.com/Matthsworld)
* [OBULOR JOY MARY](https://www.linkedin.com/in/joy-obulor-651870235/)
* [PAUL DIVINE OSINACHI](https://www.linkedin.com/in/divine-paul-911981232/)

