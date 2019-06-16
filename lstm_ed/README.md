### Anomaly Prediction using lstm encoder decoder

*Reference: The model is take from https://github.com/KDD-OpenSource/DeepADoTS and is further modified to suit needs of this project  

*src/algorithms/ has model files  
*src/data_collection/ has scripts used to collect data from RUBIS broker  
*src/online_prediction/ has scripts to detect anomalies on latest data using pretrained model  
*src/report_generation/ has scripts to generate prediction tags/scores for anomalous_data and then get_reports.py to generate results  
*src/training/ has script to train the model  


*/data has anomalous_data used for generating results and training_data used for generating models  
*/figures has the roc/pr curves generated  
*/reports have generated reports and accuracy, precison, recall etc scores in scores_* files  
