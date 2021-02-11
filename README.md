## Project title
Scaping the information you need in your daily life with Python.

## Motivation
To solve the inconvenience of daily life by scraping information at once that we have to check on differnet sites every day.

## Installing
1. pip install requests  
Connected to the site by using requests module in order to get response from server.   
Following are the sites.  
  -
  -
  -
  -
  
2. re  
To find the string (tag element) starting with certain character.

3. pip install beautifulSoup4
To get the needed tag element from HTML code.

## Code
Created 4 functions. Following is the explanation of the core code for each function.
1. def scrape_weather()  
~~~
    curr_temp=soup.find("p", attrs={"class":"info_temperature"}).get_text().replace("도씨", "")
~~~

~~~
    morning_rain_rate=soup.find("span", attrs={"class":"point_time morning"}).get_text().strip()
~~~

~~~
   dust=soup.find("dl", attrs={"class":"indicator"})
~~~

~~~
   pm10=dust.find_all("dd")[0].get_text() 
~~~


## Running the tests


