import pandas as pd
from flask import Flask , render_template , request , jsonify
from bs4 import BeautifulSoup as bs
from urllib.request import urlopen as urReq
url="https://www.knowledgehut.com/blog/data-science/data-scientist-future"
html=urReq(url=url)
soup=bs(html)
title=soup.title
print(title.text)
print(title)
links=soup.find_all("a",href=True)
for i in links:
    print(i["href"])
data=[]
allrows=soup.find_all()
for rows in allrows:
    row_list= rows.find_all()
    datarow=[]
    for cell in row_list:
        datarow.append(cell.text)
    data.append(datarow)
print(data)
df=pd.DataFrame(data)
print(df.head)
df.head()
df.info()
