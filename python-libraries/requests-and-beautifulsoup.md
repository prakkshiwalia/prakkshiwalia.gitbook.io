# Requests & BeautifulSoup

## Requests - API Data Fetching

Use Case: Automate the retrieval of competitor pricing, review or analytics data. It fetches the real-time data from  APIS for market research.&#x20;

```
import requests

response = requests.get("https://api.example.com/product-data")
print(response.json()) 
```

## BeautifulSoup - Web Scraping

Use Case: Extract competitor pricing, customer feedback, or industry trends. This helps in automating data collection for competitive analysis.&#x20;

Code Breakdown:

* bs4 is BeautifulSoup used for web scraping to get specific titles, links and paragraphs.
* requests is a python lib used for sending HTTP requests to websites.&#x20;
* .get is a function is used in requests lib to request for asking for the HTML content of the page.&#x20;
* BeautifulSoup(response.text, "html.parser") reads and understands the HTML (or even JSON) content inside response.text  into a structure that Python can understand and work with. Soup = stores the parsed HTML in this variable.&#x20;
* print(soup.title.text) - title fetches the \<title> tag inside the HTML. .text extracts the text content inside the \<title> tag and print displays the extracted text on the screen.&#x20;

Note: "html.parser" is a built-in parser in Python to extract data from web pages easily (like titles, links, reviews etc) in structures such that python reads and processes HTML code easily and fetches its elements as and when asked for.&#x20;

```
from bs4 import BeautifulSoup
import requests

response = requests.get("https://example.com/reviews")
soup = BeautifulSoup(response.text, "html.parser")
print(soup.title.text)

#-------------------------------------------------#

#BeatifulSoup converts the raw HTML into a structured object, making it easy to search.
soup.title  # Finds the <title> tag
soup.body   # Finds the <body> tag
soup.p      # Finds the first <p> (paragraph) tag
```
