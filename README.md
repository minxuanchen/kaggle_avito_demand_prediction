# Avito Demand Challenge Kaggle Competition
### Submission by Huilin Cai, Minxuan Chen, Jordan Fischer and Parisa Mofakham
#### The final submission can be found under team name HMJP at: 
* https://www.kaggle.com/c/avito-demand-prediction/submissions?sortBy=date&group=all&page=1


#### Model building
##### Data preprocessing was carried out in several steps: 
* a. Base preprocessing 
* b. Keywords generation 
* c. Image features 
* d. Text polarity 
* e. Geographic features 

#### Various Base models were built using newly processed data 
* a. Neural Network 
* b. XGBoost 
* c. Ridge (L2 regularization) 
* d. Recurrent Neural Network
      - note that (f) does not include the same data preprocessing as the other base models (all preprocessing is included in the same file) 

#### Intermediary models were created using both base models from (2) and select features from the preprocessed data 
* a. Stacked LightGBM combining base models (a), (b), and (c) from (2) and select features from preprocessed data 
* b. LightGBM using base model (c) from (2) and select features from preprocessed data 
* c. Categorical LightGBM using base model (c) from (2) and select features from preprocessed data 

#### Final Blended model 
* a. Blended model using intermediary models (a), (b) and (c) from (3), and base models (b), (c), (d), (e), and (f) from (2)
