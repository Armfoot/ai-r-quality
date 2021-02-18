# AI-R-Quality

Final project for the Building AI course.

## Summary

This Machine Learning solution aims to provide a Predictive Air Quality System for different pollutants concentrations in any chosen date in a given region.

![File Charter screenshot: data from Olivais on September 2019](https://github.com/Armfoot/file_charter/raw/master/img/2019_Sep-Olivais.png)
> Possible prediction data combined and depicted through [File Charter](https://github.com/Armfoot/file_charter)

## Background

For any a given location, pollutants concentration predictions on:
* _Past dates_ allow comparison of measured data or completion of gaps corresponding to missing data (non-measured intervals);
* _Future dates_ allow authorities to schedule warnings and deploy measures in advance to prevent health hazards on populations.

## How is it used?

A supervised learning approach is used to train a model based on reliable records from different air quality measuring stations. 

Prediction trends may be analyzed by authorities to determine periods of environmental safety or risk in order to, for example:
* recommend inhabitants of a given region to avoid exposure to outdoors air during certain days or hours of a day;
* assess probable pollutants concentrations when a measuring station fails to provide data in a certain time interval.

Model training should ideally be performed exclusively on real data provided by the measuring station of the region where predictions are to be made. If not possible, a K-neighbors approach alternative can be taken with data provided by stations in nearby regions.

## Data sources and AI methods

Training data may be provided by any official source, such as [qualar.apambiente.pt](https://qualar.apambiente.pt).

Pre-processing to clean up irregular measures or to standardize the source files to feed the model may be required. [Pre-processed files used in File Charter](https://github.com/Armfoot/file_charter/tree/master/data) may be used as a starting point.

Linear and logistic regression are appropriate methods to consider in the development of models, due to the regression nature of this problem.
Cross-validation may avoid overfitting issues in the application of these trained models.

## Challenges

Predictions depend on the amount of available data to train the model for a particular region and may be affected by random environmental changes.

**Disclaimer**: this solution **will not provide accurate assessments of environmental pollutants concentrations** for any given time and/or region and therefore we are not liable and we do not assume any responsibility if predictions obtained are used to guide real-world analysis and risk assessments.

## What next?

Asking the data source provider to have standardized files of measured data following documented rules (e.g. using -1 as a value when concentration measuring fails) will be beneficial to facilitate model training and establish a solid standard basis from which providers can rely upon for sharing their data.

With repeated applications/analysis and training of models, evaluating status or discovering flaws in measuring stations might be feasible and useful to source providers to recalibrate measuring apparatus.

Cooperation with local governments may facilitate usage of predictions to benefit communities through environmental risks assessments.

## Acknowledgments

Data visualization supported by [file_charter (Github project)](https://github.com/Armfoot/file_charter) / [Apache License 2.0](http://www.apache.org/licenses)
