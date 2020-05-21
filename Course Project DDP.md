Course Project DDP: Predict Sepal Length from Sepal Width
========================================================
author: Griffin Winton-LaVieri
date: 5/21/20
autosize: true

Three Species in iris dataset
========================================================
Might expect the relationship between Sepal Length and Sepal Width to differ for 3 species in iris dataset

- Setosa
- Versicolor
- Virginica


Construct Seperate Datasets by Species and Build Simple Models
========================================================


```r
data("iris")
  setosa<-iris[iris$Species=="setosa",]
  versicolor<-iris[iris$Species=="versicolor",]
  virginica<-iris[iris$Species=="virginica",]
  
  model1<-lm(Sepal.Length~Sepal.Width,data=setosa)
  model2<-lm(Sepal.Length~Sepal.Width,data=versicolor)
  model3<-lm(Sepal.Length~Sepal.Width,data=virginica)
```

Predict Sepal Length from Sepal Width
========================================================
Setosa with Sepal width of 3

```r
predict(model1,newdata=data.frame(Sepal.Width=3))
```

```
      1 
4.71047 
```
Versicolor with Sepal width of 3.5

```r
predict(model2,newdata=data.frame(Sepal.Width=3.5))
```

```
       1 
6.567507 
```


Shiny App Provides these Calculations
==========================================
- Thus is useful
- This is the 5th slide
- Thanks, Folks!










