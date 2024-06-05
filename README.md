import requests
from bs4 import BeautifulSoup

# Step 1: Send an HTTP request to the URL
url = "https://ai.google/"
response = requests.get(url)

# Step 2: Parse the HTML content using BeautifulSoup
soup = BeautifulSoup(response.content, "html.parser")

# Step 3: Extract the data
# Let's say we want to extract all the text inside paragraph tags (<p>)
paragraphs = soup.find_all('p')

for paragraph in paragraphs:
    print(paragraph.text)
