# Processing Times

The project: https://kellywaldro.github.io/processing-times/

This project scrapes the processing times for Canadian Permanent Residency applications (i.e. applications under the "Economic Migration" classes) from the official [IRCC website](https://www.canada.ca/en/immigration-refugees-citizenship/services/application/check-processing-times.html).

Why is this useful? 

- To have a better idea of how long you can expect to wait for a response on an application. (The IRCC website doesn't show a record, only the estimated time for that given week - and these often fluctuate.)

- To compare times between different PR programs.

# Method 

- `scrape.ipynb` scrapes the IRCC website using **Playwright** and **BeautifulSoup**. 
- `clean.ipynb` cleans the data and plots it on an interactive chart using **Bokeh**. The chart is saved as `plot.html` (with `plot.js`, too)

# The Data 

- For this prototype, I have used dummy data. 
- Going forward, the output from `scrape.ipynb` is saved to individual csv files in the `data` folder. 
    For example, the collected times for the Quebec Skilled Workers program are saved in `Skilled_workers_(Quebec).csv`
- The compiled data (with times for every program) is saved to `econ_migration_processing_times.csv`

# What I learned 

- More about scraping. I had a hard time getting this to work (I suspect it's because of dynamic classes on the page). Also because there are 2+ dropdowns for each program. 
- Conceptualizing a database. I also spent a long time figuring out how best to store the information and reorganize it accordingly. 
- Stretched myself with Bokeh. This was new to me. Baby steps in learning how JS works. 

# Things to fix + expand 

Things to fix 

- Need to address times that are given in weeks, not months. 
- Fix loop so that times with "Not Enough Data" aren't just removed.
- Need to get each line on the chart with appropriate button. 

Going forward: 

- The idea is to flesh this out to have more visa programs included. 
- I also just need to sit and wait! The data only updates weekly, so I have to wait to see how it shapes out. 



