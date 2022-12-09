# Webscrapping
#In this repository I have write a code for webscrapping.

#Install All the requirements
pip install requests
pip install bs4
pip instal html5lib
import requests
from bs4 import BeautifulSoup
url="Paste URL here"

#step 2: Get the HTML
r=requests.get(url)
htmlContent=r.content
print(htmlContent)

#step2:parce the html
soup=BeautifulSoup(htmlContent, 'html.parser')
print(soup.prettify)

#step3:HTML Tree traversal
title=(soup.title)
print(title)

#type of title
title=(soup.title)
print(type(title))

#get all the paragraphs from the page
paras=soup.find_all('p')
print(paras)

#get all the achors tag from the page
anchors=soup.find_all('p')
print(anchors)
