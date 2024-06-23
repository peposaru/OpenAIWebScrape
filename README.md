# OpenAIWebScrape

COMPUTER SYSTEMS OF EVERY MAJOR COMPANY SCRAPER

This tool is designed to collect data on every computer system produced by major companies. 
It leverages OpenAI to gather and assign data to specific data points automatically.

Without OpenAI
    Without using OpenAI to populate the data automatically, you would need to:
    
        -Identify elements/selectors for each site and update them if the HTML is dynamic (like on Amazon).
                -Manually figure out elements/selectors for each of the ~45 data points.
                -This process cannot be automated with OpenAI.
        -Use Selenium and BeautifulSoup for web scraping.
        -Potentially figure out an API for each site.
        -Gather specific elements/selectors for:
            -45 data points
            -15 sites
            -50 products per site
            
This results in **33,750 combinations** (assuming elements/selectors differ for each product on the same site). 
This doesn't include figuring out variations of the same product on the same page.

With OpenAI
    Using OpenAI simplifies the process:
    
        -Input a concise prompt with as few tokens as possible.
        -Manually input the list of products.
            -No consistent way was found to accurately scrape all products from a product page, so this must be done manually.
            -This process can take about 5-10 hours, depending on the number of products.
        -OpenAI responds with text in CSV format, which is automatically written to a text file.
            -This can be converted into a CSV data file for further use.
