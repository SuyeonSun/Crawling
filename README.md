## Project title
Scaping the information you need in your daily life with Python.

## Motivation
To solve the inconvenience of daily life by scraping information at once that we have to check on differnet sites every day.

## Installing
1. pip install requests  
Connected to the site by using requests module in order to get response from server.   
Following are the sites.  
  - https://search.naver.com/search.naver?where=nexearch&sm=top_hty&fbm=0&ie=utf8&query=%EC%84%9C%EC%9A%B8+%EB%82%A0%EC%94%A8   
  - https://news.naver.com/   
  - https://news.naver.com/main/list.nhn?mode=LS2D&mid=shm&sid1=105&sid2=230   
  - https://www.hackers.co.kr/?c=s_eng/eng_contents/I_others_english&keywd=haceng_submain_lnb_eng_I_others_english&logger_kw=haceng_submain_lnb_eng_I_others_english   
  
2. import re  
To find the string (tag element) starting with certain character.

3. pip install beautifulSoup4
To get the needed tag element from HTML code.

## Code
Created 4 functions. Following is the explanation of the core code for each function.
1. def scrape_weather()  
~~~
    curr_temp=soup.find("p", attrs={"class":"info_temperature"}).get_text().replace("도씨", "")
~~~
To get the current temperature, find "info_temperature" class in < P > tag and get text. Use replace( ) function to delete the word "도씨".  

~~~
    morning_rain_rate=soup.find("span", attrs={"class":"point_time morning"}).get_text().strip()
~~~
To get the morning rain rate, find "point_time morning" class in < span > tag and get text. Use strip( ) function to remove blank.

~~~
   dust=soup.find("dl", attrs={"class":"indicator"})
~~~

~~~
   pm10=dust.find_all("dd")[0].get_text() 
~~~
To get the brown smog rate, find "indicator" class in < dl > tag. Find all the < dd > tag in < dl > tag and select the first index. 


## Running the tests
![img1](https://user-images.githubusercontent.com/77823761/108455506-b8321580-72b1-11eb-821d-6dccf4992958.PNG)

