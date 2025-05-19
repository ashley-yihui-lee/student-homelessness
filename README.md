# Student Homelessness in NYC Public Schools

This repository contains the data, code, and analysis for a project investigating the relationship between student demographics and housing instability in New York City public schools, with a particular focus on students living in temporary housing.

## Project Overview

The goal of this project is to identify which student populations are more vulnerable to homelessness and which schools may be under- or over-serving students in temporary housing. The analysis uses regression modeling to explore the connection between student demographics (e.g., English Language Learner status, race, and poverty levels) and the percentage of students in temporary housing across schools.

## Files and Structure

- `2021.csv`, `2022.xlsx`, `2023.xlsx`, `2024.xlsx`: Student housing data from the NYC Department of Education
- `2024-demographic.csv`: School-level demographic data
- `school-2024.csv`: Merged dataset used for regression analysis
- `grad.csv`: Graduation outcome data for NYC high schools
- `linear-regression-school.ipynb`: Notebook for school-level regression analysis
- `grad.ipynb`: Notebook for regression on graduation rates and homelessness
- `README.md`: This file

## Methodology Summary

School-level housing data was merged with demographic data by DBN (school code). A multiple linear regression model was used to estimate which factors predict higher rates of student homelessness. Variables tested include:

- % White students (as a proxy for racial majority presence)
- % Hispanic students
- % Students in poverty
- % English Language Learners (ELL)

The strongest predictor was ELL status: schools with higher ELL populations also had significantly higher rates of students living in temporary housing.

A second regression explored whether schools with higher homelessness rates also had lower graduation rates. Results suggest a modest but statistically significant negative relationship.

## Key Findings

- ELL students are particularly vulnerable to housing instability.
- The model explains 44.5% of the variation in homelessness across schools.
- Residual analysis highlights schools that significantly over- or under-perform expectations, pointing to potential leads for further reporting.

## Story Leads & Future Work

- Interview schools with both high ELL and homelessness rates
- Investigate schools with large positive or negative residuals to explore support gaps or best practices
- Consider incorporating student disciplinary data in future work
- Explore admission or retention barriers for students in temporary housing
