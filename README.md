# Arcelo_mittal

### General description

This project is developed for Arcelor-mittal, a company based in Belgium.
In this project, an algorithm is developed to determine whether there is 
a constriction or not on a steel coil based on B3, B4, and B5 measurements.
Then a model is developed to predict constriction.

### Algorithm for detection of Constriction

The measurement taken at B3, B4, and B5 are not taken at the same point, hence
we don't have the same length in a set of (length, width), which makes it difficult
to compare the width of B3, B4, and B5. To tackle that we first grouped the dataset
to the int(length) and aggregated them by getting their average, which makes 
comparing B3, B4, and B5 measurements easy. Then we get a new measurement B3B4 
which is the mean of B3 and B4. And we take the absolute value of the difference
between B3B4 and B5 to determine the width difference. Finally, we count the
number of data points in which the difference is greater or equal to 5.
Our algorithm detects a coil as constriction if the count is greater than or 
equal to 6, no constriction if the count is 0, and 'not sure if the count is between 
0 to 6.

So for analysis and modeling, we only use the coils that are determined as 
constriction or not. 

Result of the algorithm:

total size of dataset:(25111, 28)
constriction: 18845
not constriction:4541
not sure: 1725

### Modeling

The dataset we have for modeling is unbalanced(18845,1725) so we downsample the 
majority class to develop our models. Different models have been tried and evaluated.
The metrics that we use for evaluation are F-score and confusion matrix as the business 
need of our client is to minimize false negative(FN) and false positive(FP).

Minimizing FN means minimizing the loss caused by manufacturing coils with constriction.
Minimizing FP keeps our client "Arcelor-mittal" in business by keeping its reputation of
manufacturing and supplying constriction-free steel coils. 



### Usage

This project is private so using the files without the consent of Arcelor mittal company is no
allowed.


## Installation

To deploy and use the project first clone it on your machine and install a virtual environment.


1. Install# arcelo_mittal

### General description

This project is developed fro Arcelor mittal, a company based in Belgium.
In this project an algorithm is developed to determine whether there is 
a constriction or not on a steel coil based on B3,B4 and B5 measurement.
Then a model is developed to predict constriction.

### Algorithm for detection Correlation

The measurement taken at B3,B4 and B5 are not taken at the same point,hence
we dont have the same length in set of (length,width), which makes difficult
to compare thewidth of B3,B4,B5. To tackle that we first grouped the dataset
to the int(length) and aggregated them by getting their average, which makes 
comparing B3,B4 and B5 measurement easy. Then we get a new measurement B3B4 
which is the mean of B3 and B4. And we take the absolute value of the difference
between B3B4 and B5 to determine the width difference. Finally we count the
number of data points in which the difference is greater or equal to 5.
Our algorithm detect a coil as constriction if the count is greater than or 
equal to 6, not correlation if count is 0 and 'not sure' if count is between 0
to 6.

So for analysis and modeling we only use the coil that are determined as 
constriction or not. 

Result of the algorithm:

total size of dataset:(25111, 28)
constriction: 18845
not constriction:4541
not sure: 1725

### Modeling

The dataset is unbalanced so we downsample the majority class and tried different 
models. we evaluate our models using different metrics..But we find out the 
confusion matrix and f-score. And we find out Random forest classifier is best
suited for modeling our dataset.


### Usage
This project is private so using the files without the consent of Arcelor mittal company is no
allowed.


### Installation

To deploy and use the project first clone it and use the deployment


1. Install virtualenv

```
pip install virtualenv
```
2. Create a virtual environment and activate it
```
virtualenv venv
> On windows -> venv\Scripts\activate
> On Linux -> . env/bin/activate

```
3. Install the necessary libraries
```
pip install -r requirements.txt
```


### Future development

* The algorithm is to be improved by applying some statistical concepts
* The dataset is also further to be preprocessed so that only features having importance used
* The models also have to be tuned further by tuning their parameters
* Different models also to be tried



#### Collaborators

Developer Team
* Olga
* Shakil
* Amanuel
* Data Engineer team

Becod coaches
* Chrysanthi
* Louis
* Vanessa

Arcelor mittal
* Thomas















