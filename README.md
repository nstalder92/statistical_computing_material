# Statistical Computing <img src='logo.png' align="right" height="200" /></a>

### Lecture Notes

#### Michael Mayer

## Organization

The lecture has six chapters: 

1. [R in Action](https://mayer79.github.io/statistical_computing_material/1_R_in_Action.html)
2. [Statistical Inference](https://mayer79.github.io/statistical_computing_material/2_Statistical_Inference.html)
3. [Linear Models](https://mayer79.github.io/statistical_computing_material/3_Linear_Models.html)
4. [Model Selection and Validation](https://mayer79.github.io/statistical_computing_material/4_Model_Selection_and_Validation.html)
5. [Trees](https://mayer79.github.io/statistical_computing_material/5_Trees.html)
6. [Neural Nets](https://mayer79.github.io/statistical_computing_material/6_Neural_Nets.html)

Chapters 3 to 6 can be summarized as "Statistical ML in Action". 

Each chapter will keep us busy for two weeks (3 hours + 1 hour exercises).
   
## Prerequisites

### Lecture material

Fetch everything by running

```
git clone https://github.com/mayer79/statistical_computing_material.git
```

in your Git console, or by downloading everything as Zip file.

### Large data

Download the large dataset "January 2022 - Yellow Taxi Trip Records" from [this page](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page) or use the direct download [link](https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2022-01.parquet).

Place it in the project subfolder "taxi/".

### Software

We will work with R version >= 4.1 and RStudio/Posit. 

In the first two chapters, we will need these additional R packages:

- tidyverse
- plotly
- insuranceData
- microbenchmark
- withr
- boot
- coin

For the remaining chapters, we further need this list:

- h2o (large package)
- arrow
- data.table
- FNN
- duckdb
- sparklyr (large package)
- rpart.plot
- ranger
- xgboost
- lightgbm
- MetricsWeighted
- flashlight
- keras (see below)

For the last chapter, we additionally need Python with TensorFlow. You can install it by running the R command `keras::install_keras()`. If the following code works, you are all set. (Some red messages/warnings are okay.)

```
library(keras)

input <- layer_input(shape = 3)

output <- input %>%  
  layer_dense(5, activation = "relu") %>%  
  layer_dense(1)

simple_model <- keras_model(input, output)

simple_model %>% 
  compile(
    loss = "mse", 
    optimizer = optimizer_adam(learning_rate = 0.2)
  )

simple_model %>% 
  fit(
    x = data.matrix(iris[2:4]),
    y = iris[, 1],
    epochs = 20,
    batch_size = 10
  )
```

## Further Material

### Books

- James, G., Witten, D., Hastie, T., Tibshirani, R. (2013). *An Introduction to Statistical Learning - with Applications in R*. New York: Springer.
- Hastie, T., Tibshirani, R., Friedman, J. (2001). *The Elements of Statistical Learning: Data Mining, Inference, and Prediction*. New York: Springer.
- Wickham, H., Grolemund, G. (2017). *R for Data Science: Import, Tidy, Transform, Visualize, and Model Data*. O'Reilly Media.
- Chollet, F., Allaire, J. J. (2018). *Deep Learning with R*. Manning Publications Co.

### Video by Trevor Hastie

- Hastie Big Data 45': https://www.youtube.com/watch?v=0EWJZIC4JxA

## Copyright

This lecture is being distributed under the [creative commons license](https://creativecommons.org/licenses/by/2.0/).

## How to cite?

Michael Mayer. Statistical Computing, Lecture notes (2023).
