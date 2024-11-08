# Diagnosis Unknown - How to Predict your Medical Bill 
_A data based approch to predict medical costs without information of the treated disease_

![Image Credit: Getty Images ](https://img.freepik.com/fotos-kostenlos/top-ansicht-krankenversicherung-form-und-brillen-mit-stethoskop-auf-holzuntergrund-business-und-gesundheitswesen-concept-savings-flat-lay-copy-raum_1921-31.jpg?t=st=1730915648~exp=1730919248~hmac=d028118b4b2ac5c4999038412214e521be274c0824c0a55b961a9caad27c66c5&w=1380)
Image Credit: freepik.com. Creator: osaba

## Introduction / Motivation
Is it possible to improve your Health with Data Science ? - Let's try!

In this Data Science project, I used medical insurance data to analyse which factors influences most the billed medical costs and 
if it is possible to predict those - without information about the treated disease.
The Input dataset is origin from health insurance. It contains information about 1338 patients with the following data points:

+ Age (18 to 64)
+ Sex (male or female)
+ BMI (Body-Mass-Index - measure to assess body weight in relation to height)
+ Children
+ Smoker
+ Region (U.S - northwest, northeast, soutwest, southeast)
+ Charges (in $)

The treated illness is not part of the data. I wanted to check, if it is still possible to predict the costs and 
what the data tells us about the importance about a healthy lifestyle and about the importance of factors which we can not influence, like the age.

The main questions of my project were:

+ **Which factors contribute the most reagring medical costs?**
+ **Can anything be said about the state of health of the residents from the data for the individual regions?**
+ **Is it possible to predict health insurance costs from the given features?**

Let's step into the data


## Part I: Which factors contribute the most reagring medical costs?

After some preprocessing of the data, I was able to calculate the correlation, which means to
make a sequence of the factors that influence the medical costs

Here you can see the result image:

![Unbenannt](https://github.com/user-attachments/assets/44c73f88-af89-4adc-bb49-119273b46c8a)


On top is "charges", our target data, which we are interested in. This has to be 1.00. The next tree listed factors are smoking, age and the Body-Mass-Index (BMI).
We can see, that smoking is by far the most important factor regaring medical costs with a calculated correlation of 0.79.
With a big gap the age is following with a calculated correlation of 0.30, followed by the BMI with 0.20. The other factors are only correlated to a very minor extent
or even negatively correlated.


## Part II: Can anything be said about the state of health of the residents from the data for the individual regions?

The provided data included the data in which of the four defined regions (northwest, northeast, soutwest, southeast) the patient lives.
In the image below, you can see the most important factors smoking, age and bmi for each region in relation to the charges.


![Unbenannt](https://github.com/user-attachments/assets/de280b93-b6a7-4870-9bdd-0ac289bfe293)
![Unbenannt](https://github.com/user-attachments/assets/16ad88a3-e393-47b3-b3b9-bd51fd8911ec)

In general, medical costs are rising with higher age, higher BMI and if you are a smoker. 
It can be seen that in the region 'southeast', people smoke more and have also highest mean BMI compared to the other regions.

Nevertheless, the data shows also that there are single individuals which influence stronly the costs for a region.


## Part III: Is it possible to predict health insurance costs from the given features?

Finally, I wanted to know, if it is possible to predict the costs for the health insurance. I splitted the dataset
into two groups. One for training the model, the other group is to testing the model and to check, how the model performs.
A calculated metric value shows us a score of 0.8 (in range 0 - 1) which is a good match for a simple try.
The data and the model are well suited for predictions of this kind.


## Conclusion

In this article, we stepped into the field of health data and medical costs.

1. We had a look on the data and checked if they are suitable for this analysis. We calculated the correlation to know which factors contribute the most to medical costs. 
2. We checked if there are specific trends in each regions and if there are region where the people, in general, pay more to medical costs
3. We build up a model to predict the costs based on the given data and checked how well the model performs.

To see more about this analysis, see the link to my Github available [here](MedicalCostPrediction.ipynb)
