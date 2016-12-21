# to_same_date
This is a python script to deal with two date series for choosing the same date

# -*- coding: utf-8 -*-
"""
Created on Fri Dec  9 10:38:41 2016

@author: Hilda
"""
'''
function : transform Date to the same
'''    

import pandas as pd
import numpy as np
data1=pd.read_csv("D:/600061.csv")       #read the data
data2=pd.read_csv("D:/600330.csv")
same_date=set(data1.date)&set(data2.date)      #choose the same date
same_date=(pd.DataFrame([same_date])).T      
newdata1=data1[data1['date'].isin(same_date[0])]       
newdata2=data2[data2['date'].isin(same_ddate[0])]                 
newdata1.to_excel('D:/600061data.xlsx',sheet_name='600061')   
newdata2.to_excel('D:/600330data.xlsx',sheet_name='600330')  
