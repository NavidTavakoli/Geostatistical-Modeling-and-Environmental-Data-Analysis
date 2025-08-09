# A Comprehensive Study on the Density of Ozone (O3) in Five European Countries
(Environmental O3 Density Analysis, Variogram Modeling, and Kriging Mapping)

![Overal](001.png)

This project presents a **comprehensive geostatistical analysis** of ground-level ozone (O₃) concentrations across five European countries: **Netherlands, Belgium, France, Switzerland, and Italy**. Using a combination of statistical analysis, variogram modeling, and kriging interpolation, the study provides insights into the spatial distribution of O₃ density for environmental monitoring and policy-making.

---

## 📌 Project Overview

Ground-level ozone is a harmful air pollutant with significant **health, ecological, and climate impacts**. The aim of this project is to:
- Assess the spatial distribution of O₃ concentrations.
- Model spatial dependencies using different variogram models.
- Generate predictive maps using kriging techniques.

---

## 🌍 Data Collection & Preprocessing

1. **Source**:  
   European Environment Agency (EEA) air quality data.

2. **Countries Analyzed**:  
   - Netherlands  
   - Belgium  
   - France  
   - Switzerland  
   - Italy

3. **Steps**:
   - Extracted ozone concentration data from monitoring stations.
   - Retrieved latitude/longitude coordinates for each station.
   - Converted coordinates to **UTM Zone 32N** using R (`sf` and `rgdal` packages).
   - Cleaned and formatted data for use in **SGems**.

4. **Dataset Summary**:
   - **Data Points**: 738  
   - **Mean O₃**: 60.22  
   - **Variance**: 127.51  
   - **Range**: 22.82 – 99.60

---

## 📊 Statistical & Geostatistical Analysis

### 1. Histogram & Descriptive Statistics
- Visualized the frequency distribution of ozone concentrations.
- Computed mean, median, variance, and range.

![Histogram](Histogram.png)

### 2. Variogram Modeling
- Evaluated **four variogram models**: Linear, Spherical, Gaussian, and Exponential.
- Modeled anisotropy with azimuths 0° and 90°.
- Cross-validated using **MSE, RMSE, MAE**.
- Selected **Exponential model** as the best fit based on lowest error metrics.

Experimental Variogram
![Experimental Variogram](Experimental_Variogram.png) 

Experimental and Fitted Variogram Exponential Azimuth 0-90
![Experimental and Fitted Variogram Exponential Azimuth 0-90](Experimental_and_Fitted_Variogram-Exponential_Azimuth_0-90.jpg)


### 3. Kriging Interpolation
- Conducted **Ordinary Kriging** and **Simple Kriging** using SGems.
- Produced:
  - O₃ concentration maps.
  - Kriging variance maps for uncertainty estimation.
 
Exponential Ordinary Kriging
![Exponential Ordinary Kriging](Exponential_Ordinary_Kriging.png) 

Exponential Ordinary Kriging variance
![Exponential Ordinary Kriging variance](Exponential_Ordinary_Kriging_var.png)

Exponential Simple Kriging
![Exponential Simple Kriging](Exponential_Simple_Kriging.png) 

Exponential Simple Kriging Variance
![Exponential Simple Kriging Variance](Exponential_Simple_Kriging_Variance.png) 


---

## 🛠 Tools & Technologies

- **R** (data processing, statistical analysis, variogram modeling)
  - Packages: `gstat`, `sp`, `sf`, `rgdal`, `raster`
- **SGems** (geostatistical mapping)
- **Excel** (result compilation)
- **GIS** concepts for spatial data analysis

---



