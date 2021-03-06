<!-- PROJECT SHIELDS -->
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

# Forecasting COVID-19 cases for the next 7 days and beyond
Accurate forecasting of COVID-19 cases is critical for epidemiological, economic and personal coping strategies, and thus it poses an important challenge for data scientists who work on time series analysis and forecasting. Here we built four different kinds of models to predict the number of COVID-19 cases for the next 
seven days in 23 countries. We trained the models based on the features that are readily available to maximize the usability of our models, namely we used Google mobility, weather, vaccination, previous cases, and temporal data (e.g. year, month, day etc.) as features. We compared performance of the models with cross validation. We conclude that the neural network model with LSTM layers outperform others, however, the XGBoost regressor model might be considered for a faster outcome with a comparable performance. 

## Motivation
<div align="center">
<a href="https://github.com/parkjlearning/covid19_forecasting/blob/main/Final_report_forecasting_COVID-19_cases.pdf">
<img src="https://github.com/parkjlearning/covid19_forecasting/blob/main/snapshots/covid19_cases_in_5_countries.png" alt="covid19 cases in 5 countries" style="width:800px;height:250px;"></a>
<div align="left">
<br>This plot illustrates dynamic time-varying patterns of COVID-19 cases (cases per million) in 5 different countries. Our goal is to construct a variety of 
models that predict future cases based on the prior cases and other relevant features like weather, datetime, mobility in various domains (e.g. parks, groceries, work places etc.). We built four different types of models: 

 1. SARIMAX 
 2. XGboost regression 
 3. Multi-layer perceptron 
 4. Long Short Term Memory networks (LSTM) 

Each model was designed to predict cases in the next 7 days per a given day. Walk forward validation for time series data was used to test model 
performance on unseen data. As there existed weeks to months gap from the train dataset to the validation or the test dataset, respectively, we could see how 
the models perform when predicting cases far ahead into the future.<br/>

## Model performance
<div align="center">
<a href="https://github.com/parkjlearning/covid19_forecasting/blob/main/Final_report_forecasting_COVID-19_cases.pdf">
<img src="https://github.com/parkjlearning/covid19_forecasting/blob/main/snapshots/model_perform_val_IE.png" style="width:800px;height:300px;"></a>
<div align="left">
<br>Once each model is trained, their performance was tested on validation and test sets that were unseen by the model during training. The figure above illustrates the actual number of cases (blue) in Ireland and the cases predicted by the LSTM model (orange) on the validation set.<br/>  
<div align="center">
<a href="https://github.com/parkjlearning/covid19_forecasting/blob/main/Final_report_forecasting_COVID-19_cases.pdf">
<img src="https://github.com/parkjlearning/covid19_forecasting/blob/main/snapshots/model_comparison.png" style="width:400px;height:300px;"></a>
<div align="left">
<br>One major motivation of this project is to compare the predictability of different models, thus we compared how the four models performed on the validation and test sets. The plot above indicates that the LSTM (red) outperformed other model variants. Also, note that the XGBoost regression model (orange) showed a comparable performance, and thus it could be a good alternative at less computational cost than the LSTM model.<br/>

## Get Started
1. Download the data:    
Data from 23 countries comprising the features and target (daily cases per million per country) of our models are preprocessed and saved in a dictionary and   pickled as 'covid_country_data.pickle'. Please follow this link to download the preprocessed data: [link_to_preprocessed_data](https://drive.google.com/file/d/143kFTTcsRNak69rHZMPf0RBxFParhxZU/view), which would be handy to kick-start building up on our codes. 
2. To install clone the repo: 
```sh
git clone git@github.com:parkjlearning/covid19_forecasting.git
```

## Additional info.
:page_facing_up: Please find the final report of this project here: [Final report](https://github.com/parkjlearning/covid19_forecasting/blob/main/Final_report_forecasting_COVID-19_cases.pdf)  
:computer: Please find the final presentation of this project here: [Final presentation](https://github.com/parkjlearning/covid19_forecasting/blob/main/Presentation_forecasting_COVID-19_cases.pdf)
 
<!-- MARKDOWN LINKS & IMAGES -->
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/parkjlearning/covid19_forecasting/blob/main/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/juncholpark
