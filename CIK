import requests
from bs4 import BeautifulSoup

ticker=input('Provide the company ticker ')
#to find individual CIK number for future parsing
URL='https://www.sec.gov/cgi-bin/browse-edgar?CIK='+ticker+'&owner=exclude&action=getcompany&Find=Search'
page=requests.get(URL)
soup=BeautifulSoup(page.content,'html.parser')
results=soup.find(id='contentDiv')
Info=results.find('span',class_="companyName")
lines=(Info.get_text())
list=lines.split()
CIK=[int(i)for i in list if i.isdigit()]
cik=str(CIK[0])

#end section for CIK parsing
