#!/usr/bin/env python
# coding: utf-8

# In[24]:


# MOBILES DATA SCRAPING FROM FLIPKART.

# importing modules
import pandas as pd
import csv
from bs4 import BeautifulSoup
import requests

# scraping the data 
url="https://www.flipkart.com/search?q=mobiles"
r=requests.get(url)
soup=BeautifulSoup(r.content,"html.parser")
titles=soup.find_all('div',class_='_4rR01T')
ratings=soup.find_all('div',class_='_3LWZlK')
reviews=soup.find_all('span',class_='_2_R_DZ')
prices=soup.find_all('div',class_='_30jeq3 _1_WHN1')
titles


# In[25]:


ratings


# In[26]:


reviews


# In[27]:


prices


# In[29]:


# scraped data converted into list
mobiletitles=[]
mobileratings=[]
mobilereviews=[]
mobileprices=[]

for title,rating,review,price in zip(titles,ratings,reviews,prices):
    mobiletitles.append(title.text)
    mobileratings.append(rating.text)
    mobilereviews.append(review.text)
    mobileprices.append(price.text)
mobiletitles

    


# In[30]:


mobileratings


# In[31]:


mobilereviews


# In[32]:


mobileprices


# In[ ]:


# saving data in csv 
d={'mobiletitles:mobiletitles,mobileratings:mobileratings,mobilereviews:mobilereviews,mobileprices:mobileprices'}
model=pd.DataFrame(d)
model.to_csv("mobilesdata.csv")


# In[33]:





# In[ ]:





# In[ ]:




