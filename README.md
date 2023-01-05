# Web Scraping Challenge

## Deliverable 1: Scrape Titles and Preview Text from Mars News

### Step 1: Visit the Website

Use automated browsing to visit the [Mars NASA news site](https://redplanetscience.com). Inspect the page to identify which elements to scrape.

![mars_news1](https://user-images.githubusercontent.com/113717031/210473842-0c585bd0-1c14-477d-a265-a721b347cf03.png)

![mars_news2](https://user-images.githubusercontent.com/113717031/210473872-cf63eb86-a263-4bd9-ac17-775fc9383a11.png)

### Step 2: Scrape the Website

Create a Beautiful Soup object and use it to extract text elements from the website.

![mars_news3](https://user-images.githubusercontent.com/113717031/210474279-c1dcacd1-d93a-408c-964f-1f0edcfceb78.png)

### Step 3: Store the Results

Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:

* Store each title-and-preview pair in a Python dictionary. And, give each dictionary two keys: `title` and `preview`. An example is the following:

  ```python
  {'title': "Mars Rover Begins Mission!", 
        'preview': "NASA's Mars Rover begins a multiyear mission to collect data about the little-explored planet."}
  ```

* Store all the dictionaries in a Python list.

* Print the list in your notebook.

![mars_news4](https://user-images.githubusercontent.com/113717031/210474296-ca3fe800-e306-4c14-90ff-046254465f59.png)

### (Optional) Step 4: Export the Data

Optionally, store the scraped data in a file or database (to ease sharing the data with others). To do so, export the scraped data to either a JSON file or a MongoDB database.

![mars_news5](https://user-images.githubusercontent.com/113717031/210474395-556870bf-ca7a-4f65-866a-ee83acfc1f73.png)

## Deliverable 2: Scrape and Analyze Mars Weather Data

### Step 1: Visit the Website

Use automated browsing to visit the [Mars Temperature Data Site](https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html). Inspect the page to identify which elements to scrape. Note that the URL is `https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html`.
      
![web_scrape1](https://user-images.githubusercontent.com/113717031/210474736-d2fa90d0-48b0-420c-a881-e133cd30bf54.png)

### Step 2: Scrape the Table

Create a Beautiful Soup object and use it to scrape the data in the HTML table.

Note that this can also be achieved by using the Pandas `read_html` function. However, use Beautiful Soup here to continue sharpening your web scraping skills.

![web_scrape2](https://user-images.githubusercontent.com/113717031/210474760-7f57e55e-cdca-4b77-a836-7c2425a9143f.png)

### Step 3: Store the Data

Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:

* `id`: the identification number of a single transmission from the Curiosity rover
* `terrestrial_date`: the date on Earth
* `sol`: the number of elapsed sols (Martian days) since Curiosity landed on Mars
* `ls`: the solar longitude
* `month`: the Martian month
* `min_temp`: the minimum temperature, in Celsius, of a single Martian day (sol)
* `pressure`: The atmospheric pressure at Curiosity's location

![web_scrape3](https://user-images.githubusercontent.com/113717031/210475014-645a9d21-f4df-4a4f-b984-f03f4fc3839e.png)

![web_scrape4](https://user-images.githubusercontent.com/113717031/210475041-6a028011-e2c1-442a-95d1-4128ab32f7f9.png)

### Step 4: Prepare Data for Analysis

Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate `datetime`, `int`, or `float` data types.

![web_scrape5](https://user-images.githubusercontent.com/113717031/210475088-a71f4baa-9b98-40aa-9317-f367ea02dfa9.png)

### Step 5: Analyze the Data

Analyze your dataset by using Pandas functions to answer the following questions:

1. How many months exist on Mars?
2. How many Martian (and not Earth) days worth of data exist in the scraped dataset?
3. What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
    * Find the average the minimum daily temperature for all of the months.
    * Plot the results as a bar chart.
4. Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
    * Find the average the daily atmospheric pressure of all the months.
    * Plot the results as a bar chart.
5. About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
    * Consider how many days elapse on Earth in the time that Mars circles the Sun once.
    * Visually estimate the result by plotting the daily minimum temperature.

![web_scrape6](https://user-images.githubusercontent.com/113717031/210475124-586e7fde-92f8-4496-92b2-39229a8be2db.png)

![web_scrape7](https://user-images.githubusercontent.com/113717031/210475139-dfbbb919-ba2a-4215-a325-4937b6049878.png)

![temp_month](https://user-images.githubusercontent.com/113717031/210475204-3d480006-ec11-4639-94b0-73984eb7c296.png)

![temp_month_ascending](https://user-images.githubusercontent.com/113717031/210475234-e4623ebe-f1b7-4c56-b322-27fe3eda08cb.png)

![web_scrape8](https://user-images.githubusercontent.com/113717031/210475247-c277eb99-cacf-41cf-bab4-3692f835bec2.png)

![atmosph_month](https://user-images.githubusercontent.com/113717031/210475258-398f1bd6-1af2-42d4-9ba0-3de4de57049e.png)

![temp_day](https://user-images.githubusercontent.com/113717031/210475270-6b03f7d2-2f40-4f8e-9b06-6deebfc9e614.png)

On average, the third month has the coldest minimum temperature on Mars, and the eighth month is the warmest. But it is always very cold there in human terms!

Atmospheric pressure is, on average, lowest in the sixth month and highest in the ninth.

The distance from peak to peak is roughly 1425-750, or 675 days. A year on Mars appears to be about 675 days from the plot. Internet search confirms that a Mars year is equivalent to 687 earth days.

### Step 6: Save the Data

Export the DataFrame to a CSV file.

![web_scrape9](https://user-images.githubusercontent.com/113717031/210476100-4447fd71-7eb7-4b91-a23f-af093a9349ef.png)

