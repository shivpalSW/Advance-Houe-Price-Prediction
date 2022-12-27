# Advance-House-Price-Prediction
<h1>About Dataset </h2>
<p>I took this dataset form kaggle url : https://www.kaggle.com/c/house-prices-advanced-regression-techniques/overview. This dataset is an Alternative to the Boston Housing Data and good fit for a Regression Project. This is the original url of the paper : http://jse.amstat.org/v19n3/decock.pdf.</p>
<p>This dataset contains a large number of features and and missing values which makes it good fit for both EDA and feature engineering along with model selection.</p>
  
  ## EDA And Feature Engineering
  <p>During EDA I explored missing values,crorelation between features along with outlier detection.I found out that some features were not normally distributed which is the main assumption of linear regression so I used log transformation to convert them. Check ames_missing_values dataset. Now During feature engineering I handled them carefully.</p>
  
  ## Training Process And Results 
  <p> I used R2 score , MAE , RMSE as an evalution score. I have also used PCA in some models because without it hyperparameter training was very computer intensive and was taking a lot of time. I was suprised to see that PCA with SVR can give accuracy same as base SVR. At last I choose gradient boost and created a pickle file. In Advance house price prediction file you will see two plots Residual,Q-Q plot these plots indicate that how good a model is when it comes to prediction.</p>
  <pre> Linear Regression : Very bad results.
        MAE :  290974305.3431166
        RMSE : 6522582702.574113
        R2 Score : -2.701079083063056e+20</pre>
        
  <pre>Lasso : 
        MAE :  20723.739185399554
        RMSE : 35000.30563860575
        R2 Score : 0.8566180914183306 </pre>
    
  <pre>Ridge : 
         MAE :  14756.804109604633
         RMSE : 27431.38808003158
         R2 Score : 0.9127040793894553</pre>
         
   <pre>ElasticNet:
         MAE :  26512.956017808694
         RMSE : 44314.05933652656
         R2 Score : 0.7703789088906651</pre>
         
   <pre>Support Vector Regressor:
         MAE :  15825.737304556542
         RMSE : 26935.8369809242
         R2 Score : 0.9052187357130085</pre>
   
   <pre>KNeighborsRegressor:
         MAE :  24030.016628658483
         RMSE : 38748.54958828487
         R2 Score : 0.7823925097024562</pre>
   
   <pre>Decision Tree Regressor:
       MAE :  23388.038488082173
       RMSE : 35893.466287142444
       R2 Score : 0.7734711929855768</pre>
       
   <pre>Random Forest Regressor:
          MAE :  16580.803262815934
          RMSE : 27261.373125521783
          R2 Score : 0.8834068902653265 </pre>
          
   <pre>Adaboost Regressor:
        MAE :  24996.42160830527
        RMSE : 39622.345823873526
        R2 Score : 0.8046637618977778 </pre>
        
   <pre>Gradient Boost Regressor:
         MAE :  15621.071836809726
         RMSE : 24374.994525927406
         R2 Score : 0.9013682963533898</pre>
         
  <p>Overall Winners : Ridge , SVR , Random Forest,Gradient boost.</p>
