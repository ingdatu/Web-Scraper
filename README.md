# Web-Scraper
## Description
This project is a Python-based web scraper that utilizes the CrossRef API to search for academic publications related to Machine Learning and career choice. The scraper retrieves metadata such as title, authors, publication year, and abstract of each article, processes the results in batches using pagination, and saves the data to an Excel file.

## Features
Search and retrieve articles from the CrossRef API.
Pagination support for large result sets.
Export data to Excel format for easy manipulation.
Retrieve metadata like the title, authors, abstract, and publication year.

## Installation
To use the scraper, you need Python installed, along with the following libraries:
requests (for handling API requests).
pandas (for handling the data and exporting to Excel).
To install these, use:

pip install requests pandas

## How to Use the Web Scraper
Clone this repository to your local machine or download the notebook file.
Open the Web_Scraper.ipynb notebook in Google Colab or Jupyter Notebook.
Run the notebook to search for publications related to Machine Learning.
The results will be saved to an Excel file named publication_results.xlsx and automatically downloaded.

## Code Functionality
The web scraper follows a sequence of steps:

## Initialization:
Constants are defined, including the search term (Machine Learning AND choice major careers), the maximum number of results, and the number of results per page.

## Execution of the Search:
The program sends a request to the CrossRef API using the search term. It retrieves results in batches (pagination) by iterating the available pages.

## Processing of Results:
The program processes the JSON response from the API, extracting key metadata like title, authors, abstract, and publication year for each article.

## Example Output
An example output might look like this in the Excel file:
| Column 1          | Column 2     | Column 3              | Column 4     | Column 5          |
|-------------------|--------------|-----------------------|--------------|-------------------|
| Row 1, Column 1   | Row 1, Column 2 | Row 1, Column 3     | Row 1, Column 4 | Row 1, Column 5   |
| Row 2, Column 1   | Row 2, Column 2 | Row 2, Column 3     | Row 2, Column 4 | Row 2, Column 5   |

## Contribution
If you'd like to contribute to this project, feel free to submit a pull request. All contributions are welcome!

## Saving Results:
The metadata is stored in a pandas DataFrame and exported to an Excel file (publication_results.xlsx).

## Error Handling:
The scraper includes basic error handling for API requests, checking the response status, and stopping the search if no more results are available.
