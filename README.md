# Crypto Automation Website
Automating on Crypto Website 
![Encoder Block](https://topcryptoanalysis.com/wp-content/uploads/2022/01/image-3-1536x628.png)
Lets find out how we can plot crypto historical prices with Python in Seaborn. To do so, we will use Cryptocompare free API to download historical crypto market data. Then, we will convert the crypto historical data in the right format 

Using :
The CoinMarketCap API is a suite of high-performance RESTful JSON endpoints that are specifically designed to meet the mission-critical demands of application developers, data scientists, and enterprise business platforms.


#API documentation :
#This example uses Python 2.7 and the python-request library.

parameters = {
  'start':'1',
  'limit':'5000',
  'convert':'USD'
}
headers = {
  'Accepts': 'application/json',
  'X-CMC_PRO_API_KEY': 'b54bcf4d-1bca-4e8e-9a24-22ff2c3d462c',
}

session = Session()
session.headers.update(headers)

try:
  response = session.get(url, params=parameters)
  data = json.loads(response.text)
  print(data)
except (ConnectionError, Timeout, TooManyRedirects) as e:
  print(e)


