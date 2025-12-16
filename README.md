# Stratified-Sampling-Sample-Size-Shiny
R Shiny application for determining required sample size and optimal allocation under stratified sampling using proportional, Neyman, and cost-optimised methods.
# Stratified Sampling – Sample Size & Allocation (R Shiny)

This repository contains an R Shiny application developed to determine the required sample size for estimating a population mean using stratified sampling techniques.

The application computes sample allocation under:
- Proportional Allocation
- Neyman Allocation
- Optimised Allocation (considering cost and time)

The tool allows users to input stratum-wise population size, variability, cost, and time, and compares how different allocation strategies affect sample size and efficiency.

---

## Methodology

Let:
- \( N_h \) be the population size of stratum \( h \)
- \( S_h \) be the standard deviation of stratum \( h \)
- \( n_h \) be the sample size from stratum \( h \)

### Proportional Allocation
\[
n_h = n \frac{N_h}{N}
\]

### Neyman Allocation
\[
n_h = n \frac{N_h S_h}{\sum N_h S_h}
\]

### Optimised Allocation
\[
n_h = n \frac{N_h S_h / \sqrt{c_h t_h}}{\sum N_h S_h / \sqrt{c_h t_h}}
\]

---

## Features
- Interactive input of stratum parameters
- Automatic sample size calculation
- Visual comparison of allocation strategies
- Variance-efficient survey design support

---

## How to Run

```r
install.packages("shiny")
library(shiny)
runApp("app.R")
