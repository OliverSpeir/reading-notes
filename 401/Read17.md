# Web Scraping

## Resources

- [Web Scrape with Python in 4 minutes](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)
- [What is Web Scraping?](https://en.wikipedia.org/wiki/Web_scraping)
- [How to scrape websites without getting blocked](https://www.scrapehero.com/how-to-prevent-getting-blacklisted-while-scraping/)
- [Video Track Amazon Prices](https://www.youtube.com/watch?v=Bg9r_yLk7VY)
- [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/)

### [Web Scrape with Python in 4 minutes](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)

- Currently Paylocked on Medium

### [What is Web Scraping? Wikipedia](https://en.wikipedia.org/wiki/Web_scraping)

- Techniques:

1. Human copy-and-paste
2. Text pattern matching
3. HTTP programming
4. HTML parsing
5. DOM parsing
6. Vertical aggregation
7. Semantic annotation recognizing
8. Computer vision web-page analysis

### [How to scrape websites without getting blocked](https://www.scrapehero.com/how-to-prevent-getting-blacklisted-while-scraping/)

- has to be performed responsibly so that it does not have a detrimental effect on the sites being scraped

- Avoid Getting Blocked:

  - Respect Robots.txt
  - crawl slowly
  - change crawl pattern periodically
  - make requests through proxies and change those proxies
  - rotate user agents and respective headers
  - use headless browser (puppeteer selenium or playwright)
  - beware of honey pot traps
  - check if website is changing their layout
  - avoid scraping data behind a login
  - use captcha solving services

- How websites detect scraping:

  - high download rate/unusually fast actions
  - repetitive tasks in consistent pattern
  - can run javascript which will tell the graphics card/cpu of user
  - honey pots (invisible links)

- How to tell if blocked:
  
  - captcha pages, content delays, frequent error responses (301,401,403,404,408,429,503)

### [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/)

- Screen Scraping Library
- Can use different parsers
- automitically converts incoming documents to unicode and outgoing to UTF8
- Can do things like find all links matching x condition
- Reddit uses beautiful soup to find image for links
