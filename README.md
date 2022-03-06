<h1 align="center">
  <br>
   <img src=https://user-images.githubusercontent.com/61688477/147778433-746a8785-ad30-4160-aed1-d74c87f22c05.jpg>
  <br>
  Analysis of Seoul Bike Demand
  <h2 align="center">
    CHMIEL Audrey & DONIER Marie  
    <br>
    ESILV | DIA 1
  </h2>
</h1> 

## Table of contents
  * [About the project](#about_the_project)
  * [Notebook](#notebook)
  * [Usage - API](#usage)
  * [Architecture](#architecture)

## About the project
### Introduction

*This project is the final project of ESILV course Python for Data Analysis* 
<br>
During this project, we had to study a CSV dataset for estimating Seoul Bike rental demand from each hour based on a panel of time and meteorological criteria. 
<br> This project concerns the dataset 'Seoul Bike Sharing Demand Data Set' that can be found here:
https://archive.ics.uci.edu/ml/datasets/Seoul+Bike+Sharing+Demand

The project contains a preliminary data cleaning, data exploration, visualizations, dimensionality reduction, data preprocessing, data modeling.
All those can be found in the jupyter notebook "Seoul_Bike_Data_Project.ipynb".

The project also includes a Flask API to make predictions.

A report is also given in PDF format. [Go to the study](../main/Report_final_ppt_CHMIEL_DONIER_DIA1.pdf)

### Tasks achieved 

The project is organized in 3 main parts: 
<br><br>
•	  A data visualization part, where we studied the links between our target variable "Bike_Count" and the other variables, using elaborate graphics made via the Python matplotlib and seaborn libraries. Once this approach was carried out, we saw that the number of bikes rented depended a lot on the Temperature and Time variables (Day, Hour, Month...) and less on some meteorological features. <br> We then cleaned up our model by removing the insignificant variables, in order to make its prediction more efficient. We also adapted our categorical features into numerical variables to make them exploitable thanks to Pandas library functions.
<br><br>
•	  The second major part of this project was the realization of predictive models based on Machine Learning using supervised regression learning methods built thanks to  the Scikit Learn library. We have carried out numerous tests by swapping the hyperparameters in order to obtain the smallest error, and therefore the best possible precision. We even try to use a neural network model by using the tensor flow library Keras.
<br><br>
•  Finally the last part of our project was to transform our model into an API. We choose to do it with Flask
 
### Conclusion
From our visualisations, we found that time variables and temperature have a strong influence on our target value. We noticed that people from Seoul tend to rent more bikes during Summer, especially during commuting hours and when the weather is warm.
<br><br>
By comparing many Machine Learning models and trying different combinations of hyperparameters, we found that the Gradient Boosting model was the best algorithm to predict Seoul bike rental demand. We also noticed that we obtained better performance scores with all the features, so we included them all in our final GB model (used for the API), in which we have 94.1% of data that fit inside the model. 
<br><br>
For more informations on the project (observations/selection of features, model selection), please go to the notebook's section below. 
 
 ## Notebook
 [Go to the study](../main/Seoul_Bike_Data_Project.ipynb)

 ## Usage - API
 The Flask API is in the notebook "Flask_application.ipynb". 
 [Go to the study](../main/Flask_application/Flask_application.ipynb)
 
 First, after opening the notebook, you need to put some files in the “content” folder :
  - You have to put the files index_accueil.html, model_grad_boosting_reg.pkl and df_bike2.pkl
  - You have to create a “static” folder. In the “static” folder, place the image bike.jpg, create a “css” folder in which you place the file style.css
  - // Be careful, the name of the folders is case sensitive, you must write the names the same way as shown below on the picture.
  ![image](https://user-images.githubusercontent.com/95496652/147863425-66063d62-4d66-4be5-8715-fc2340f13ca2.png)

 
 Then after that, you must execute all cells.
 When you run the application cell (the last one), three internet links will appear. Click on the second to access the API.
 
 ![tempsnip](https://user-images.githubusercontent.com/95496652/147863512-7b923101-a5f8-4fbf-b994-535484f5d57e.png)

![image](https://user-images.githubusercontent.com/95496652/147863518-c69a9ffe-b2ce-4b2f-8df4-61af57dd8caa.png)


You can then fill in the required information and get the prediction by clicking on the "Get the bike count prediction" button.


 
 ## Architecture
 
![image](https://user-images.githubusercontent.com/95496652/147891121-2706345a-4465-4f3e-a591-e00949dc1a79.png)

-------------------------
