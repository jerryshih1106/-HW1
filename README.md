使用LSTM  
將2019一月~2020十二月   
全部的尖峰供電、負載、備轉容量、備轉容量率、工業用電以及民生用電整合  
以前面30天預測之後的30天  
最後再output其中前面7天的資訊  
目前是以2021年的1/1到1/30做為測試資料  
predict後面7天 

loss:0.0072, vl_loss: 0.0084  RMSE:304.9612084582683 (1/31-2/6)   
指令為 python app.py --training 2021年test.csv --output submission.csv      
---------------------------------------------------------------------[20210312]   
考慮到近期的資訊只有備轉容量與備轉容量率      
新增另一個LSTM   
將其與前面model整合      
predict前多乘上一個參數整合   
RMSE:110.33170284218629 (3/9-3/15)      
---------------------------------------------------------------------[20210319] 
