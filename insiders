#code as of 6.20.20
#begin section for insider transactions
#section for transactions
URL='https://www.sec.gov/cgi-bin/own-disp?action=getissuer&CIK='+cik
page=requests.get(URL)
soup=BeautifulSoup(page.content,'html.parser')
results=soup.find(id='transaction-report')
lines=(results.get_text())
    
#section for owners
results=soup.find('table',border='1',cellspacing='0',cellpadding='3')
lines=(results.get_text())
print(lines)
