This project pulls data from two main sources:

1. Table of Nobel Laureates in Literature from Wikipedia
	(https://en.wikipedia.org/wiki/List_of_Nobel_laureates_in_Literature)
2. Novelists and works data scraped from Fantastic Fiction
	(https://www.fantasticfiction.com/)

The "data_and_collection_scripts" folder contains all of the files that deal with collecting and preprocessing data. The actual data files are created and stored within the "data" subfolder.

By default, the data folder contains files that are current for 2025. To see the project, you may simply run the report_notebook.ipynb file. However, if you wish to update the data or simply want to run the collection/preparation scripts, run them IN THIS ORDER:

1. wiki_data_collection.ipynb
2. wiki_data_preparation.ipynb
3. works_data_collection.ipynb
4. works_data_preparation.ipynb

This specific order is necessary because "works_data_collection.ipynb" uses fields from the transformed Wikipedia table in order to scrape data from the Fantastic Fiction website. Note that "works_data_collection.ipynb" may take a few minutes to run completely, since there are time.sleep() calls intended to space out request calls to the webpage. Since both data collection scripts rely on reading active HTML pages from the internet, they may become unstable in the future.