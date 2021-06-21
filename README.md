# Data Analysis for US Health Insurance
## Propose
- We want to analyze the data of US Health Insurance and analyze the factors.
- We wanted to make a meaningful interpretation of the data.

## Dataset
- Data Information

![Dataset](https://user-images.githubusercontent.com/63955072/122763544-68a03c80-d2d9-11eb-9222-39717dbff47f.png)

## Data Preprocessing
- Change dummy value to 0, 1

<img width="602" alt="Data Preprocessing 1" src="https://user-images.githubusercontent.com/63955072/122764199-2fb49780-d2da-11eb-9e72-5dfae5e724a1.PNG">

- One hot encoding

<img width="697" alt="Data Preprocessing 2" src="https://user-images.githubusercontent.com/63955072/122764270-48bd4880-d2da-11eb-97f2-cc9150190696.PNG">

## Method
- Determining Dependent and Independent Variables

<img width="586" alt="Data Variable" src="https://user-images.githubusercontent.com/63955072/122764859-dd27ab00-d2da-11eb-93d5-e695981e4a6d.PNG">

- Variable Correlation

<img width="586" alt="Data Variable" src="https://user-images.githubusercontent.com/63955072/122765079-16f8b180-d2db-11eb-8de4-aab4c1d5953a.PNG">

## Analysis
### Linear Regression
- Relationship between actual and predicted measurements

![regression](https://user-images.githubusercontent.com/63955072/122765605-a30ad900-d2db-11eb-8272-51202dd77903.png)

- Analyze Linear Regression for Variables
> The older you are, the higher the premium. <br/>
> The higher the bmi measurement score, the higher the premium. <br/>
> The more children there are, the higher the insurance premium. <br/>
> If you smoke, the premium goes up. <br/>
> In the United States, premiums tend to be high in the order of northeast, northwest, southwest, and southeast. <br/>

![변수 regression](https://user-images.githubusercontent.com/63955072/122765865-e6654780-d2db-11eb-9db3-c3aeec40ccfa.png)

- Determine if multicollinearity

![multicollinearity](https://user-images.githubusercontent.com/63955072/122766703-d0a45200-d2dc-11eb-8924-5b83bd73b675.png)

- We verify the fit of linear regression.
> Determines fit for linear regression by obtaining value f <br/>

### Regression Tree

- Setting max depth
> The deeper the max depth, the higher the train accrual, but at some point the test accrual drops. <br/>

<img width="876" alt="Regression Tree 1" src="https://user-images.githubusercontent.com/63955072/122768696-cf742480-d2de-11eb-92a5-7473dbcf6db6.PNG">

- Regression Tree with max depth of 4

![Regression Tree 2](https://user-images.githubusercontent.com/63955072/122769690-bddf4c80-d2df-11eb-8c44-a5773024dae1.PNG)

- Adjust Hyper parameters
> min samples leaf: 1 -> 20 <br/>
> min samples split: 2 -> 30 <br/>
> max depth: 4 -> 1000 <br/>

<img width="377" alt="Regression Tree 3" src="https://user-images.githubusercontent.com/63955072/122770157-21697a00-d2e0-11eb-8fea-0a636db77755.PNG">

- Feature Importance
> The smoker variable has been shown to be the most important. <br/>
> In fact, the average premium for smokers is 3.7 times higher than the average premium for non-smokers. <br/>

![Regression Tree 4](https://user-images.githubusercontent.com/63955072/122770242-3940fe00-d2e0-11eb-9e8c-97f077c1e30a.PNG)

### Decision Tree
- Built Decision Tree
> Visualize with max depth of 4 <br/>
> Built with Entropy <br/>

<img width="873" alt="Decision Tree 1" src="https://user-images.githubusercontent.com/63955072/122773012-e87ed480-d2e2-11eb-8721-a3f823b7f4b1.PNG">

> At a glance, you can see the distribution of trees according to premiums. <br/>
> The orange, the younger you are and the fewer children you have. <br/>
> The more orange, the lower the bmi, and most non-smokers. <br/>
> The more purple you are, the older you are and the more you have children. <br/>
> The more purple it is, the more bmi it is, the more smokers it is. <br/>

![Decision Tree Visualization](https://user-images.githubusercontent.com/63955072/122771404-5c1fe200-d2e1-11eb-9d62-0b5656f4296e.png)

### Gradient Boosting
- Built Decision Tree by Using Gradient Boosting
> Visualize with max depth of 4 <br/>

<img width="832" alt="Gradient Boosting 1" src="https://user-images.githubusercontent.com/63955072/122773484-5c20e180-d2e3-11eb-8e0e-0d04c8200ec8.PNG">

## Conclusion
- All three are given the same number of max depth values.
- test accuracy: Gradient Boosting > Regression Tree > Linear Regression
- The smoker variable has the highest importance.
