# EDA: Salary Data

## INTRODUCTION
This is the repo about Exploratory Data Analysis for employee salary in a company.
Furthermore, the salary data breakdown is specifically made for Income Tax report preparation.
Some features has been modified to protect the confidentials.

## TECHNICAL
Language: R (code is written in Rmd file)

Libraries:
* tidyverse
* dplyr
* readxl
* scales
* descr

## DATASET
The dataset columns is in Indonesian, and I'm not changing column names. So here's the rough translation:
- `Masa Perolehan Awal` = Employee join month
- `Masa Perolehan Akhir` = Employee exit month
- `NIP` = Employee identification number
- `Jenis Kelamin` = Gender
- `Status PTKP` = Marriage status: K = Married, TK = Not Married
- `Jumlah Tanggungan` = Amount of dependence
- `Gaji Pokok dan Tunjangan Tetap` = Net Salary and Fixed Allowance
- `Tunjangan lain (Variabel)` = Other Allowances
- `JKK & JKM & BPJS Kesehatan` = Health Insurance
- `THR dan Bonus` = Bonus / Holiday Allowance
- `Tunjangan PPh` = Tax Allowance
- `Jumlah Penghasilan Bruto` = Gross Income

## ANALYSIS POINTS
1. Check whether any duplicate data based on NIP.
2. Check Turnover rate based on the amount of employee out before end of year. 
3. Create new column `PTKP` based on `Status PTKP` and `Jumlah Tanggungan` group
4. Create new column `PTKP_to_Bruto`, to make conditional output: whether the Gross Income is over or under PTKP amount.
5. Single, Married, or Divorced? Check the marital status based on `Status PTKP` and `Jumlah Tanggungan` condition.
6. The Barchelors!!! Find the number for those who is still single, and make income over IDR 100million a year.
7. Check correlation between gender and salary, using Dot Plot visualization.
8. Lastly, check correlation between Gender and Marriage Status, using CrossTable analysis. 

## NOTES:
1. `PTKP` is the maximum amount of income that will not be deducted for tax.
2. In actual, calculation for Income Tax report is more complicated. Here we did some simplification for the practice sake.
