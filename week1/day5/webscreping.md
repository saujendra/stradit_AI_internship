Web Scraping Using Python 
++++++++++++++++++++++++++++++ 
What is web scraping? 
Web scraping is the process of extracting data from websites automatically. 
Python is widely used for web scraping because of its easy syntax and 
powerful libraries like BeautifulSoup, Scrapy and Selenium. 
Web Scraping Works: 
1) Sends request to website  
2) Downloads HTML  
3) Extracts required data  
4) Saves data (CSV, JSON, database) 
web scraping process  step is: 
1. Identify target website  
2. Inspect webpage HTML  
3. Send HTTP request  
4. Get webpage response  
5. Parse HTML -beutifulsoup 
6. Extract required data  
7. Clean data  
8. Store data  
9. Handle errors and pagination 
Real life example: 
Amazon Product Scraper 
Process: 
1. Open product page  
2. Send request  
3. Parse HTML  
4. Find:  
a. product title  
b. price  
c. rating  
5. Save in CSV 
Requests Module: 
The Python requests module is one of the most popular libraries for making HTTP                          
requests. 
• Access websites  
• Download webpages  
• Call APIs  
• Send data to servers  
• Upload files  
• Handle authentication  
• Manage sessions/cookies 
pip install requests installing  
What is HTTP? 
Browser → Request → Server 
Server → Response → Browser 
import requests >> import the module 
>>>>Python requests Module Methods 
1. GET Method 
Used to retrieve data from server. 
Ex: 
response = requests.get( 
"https://example.com" 
) 
print(response.text) 
Uses: 
• Open webpages  
• Fetch API data  
• Download HTML 
2. POST Method 
Used to send data to server.  
data = { 
"username": "admin", 
"password": "123" 
} 
response = requests.post( 
"https://httpbin.org/post",) 
data=data 
) 
Uses 
• Login forms  
• Registration forms  
• Uploading data 
3. PUT Method 
Used to update existing data completely. 
import requests 
data = { 
"name": "John" 
} 
response = requests.put( 
"https://httpbin.org/put", 
data=data 
) 
Uses 
• Update records  
• Replace database entries 
4. PATCH Method 
Used for partial updates. 
import requests 
data = { 
"name": "Mike" 
} 
response = requests.patch( 
"link", 
data=data 
) 
print(response.text) 
5. DELETE Method 
Used to remove data. 
import requests 
response = requests.delete( 
"https://httpbin.org/delete" 
) 
print(response.text) 
Uses 
• Delete user  
• Remove records  
• Delete resources  
6. HEAD Method 
Gets only headers, not body content. 
import requests 
response = requests.head( 
"https://example.com" 
) 
print(response.headers) 
Uses 
• Check content type  
• Check file size  
• Verify webpage exists  
7. OPTIONS Method 
Shows supported methods of server. 
import requests 
response = requests.options( 
"https://httpbin.org" 
) 
print(response.headers) 
8. Request Method (Generic) 
You can use one generic method. 
import requests 
response = requests.request( 
method="GET", 
url="https://example.com" 
) 
print(response.st 
auth on 
files l 
10. GET with Parameters 
params = { 
"q": "python" 
} 
response = requests.get( 
"https://example.com/search", 
params=params 
) 
print(response.url) 
11. POST with JSON 
data = { 
"name": "John", 
"age": 25 
} 
response = requests.post( 
"https://httpbin.org/post", 
json=data 
) 
print(response.json()) 
12. Using Headers 
headers = { 
"User-Agent": "Mozilla/5.0" 
} 
response = requests.get( 
"https://example.com", 
headers=headers 
) 
13. Upload Files 
files = { 
"file": open("test.txt", "rb") 
} 
response = requests.post( 
"https://httpbin.org/post", 
files=files 
) 
14. Authentication 
from requests.auth import HTTPBasicAuth 
response = requests.get( 
"https://example.com", 
auth=HTTPBasicAuth("user", "pass") 
) 
1. Beautiful Soup (BS4)  
Beautiful Soup is a Python library used for parsing HTML and XML 
documents. It helps programmers extract data from webpages easily. 
Beautiful Soup creates a parse tree from webpage source code that 
allows easy navigation and searching of webpage elements. 
Purpose of Beautiful Soup 
• Extracting webpage data  
• Reading HTML structure  
• Navigating webpage tags  
• Searching webpage elements 
disadvantages of Beautiful Soup 
No JavaScript Execution 
Cannot load content generated dynamically using JavaScript. 
No Browser Automation 
Cannot: 
• Click buttons  
• Fill forms  
• Scroll pages  
• Login automatically 
2. Selenium: 
Selenium is an open-source browser automation framework used to 
automate web browsers. 
It controls browsers programmatically and simulates real user actions. 
Purpose of Selenium 
Main purposes: 
• Browser automation  
• Dynamic website scraping  
• Web application testing  
• User interaction simulation  
Working of Selenium 
Step-by-Step Working 
1. Launch browser  
2. Open webpage  
3. Execute JavaScript  
4. Interact with webpage  
5. Extract webpage data 