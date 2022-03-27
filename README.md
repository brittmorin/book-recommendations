# book-recommendations
Using web-scraped Goodreads dataset to find similar books.
The notebook in this repository creates a book recommendation function when a title present within the data is entered.

THE DATA : The dataset, 'Complete Book Graph' was sourced from Menting Wan and the UCSD Book Graph site at https://sites.google.com/eng.ucsd.edu/ucsdbookgraph/home
Information about the data and how it was collected can be found at https://github.com/MengtingWan/goodreads and from the following papers:
Mengting Wan, Julian McAuley, "Item Recommendation on Monotonic Behavior Chains", in RecSys'18. [bibtex]
Mengting Wan, Rishabh Misra, Ndapa Nakashole, Julian McAuley, "Fine-Grained Spoiler Detection from Large-Scale Review Corpora", in ACL'19. [bibtex]

IMPORTING THE DATASET: The file (goodreads_books.json.gz) was downloaded and saved in a collection on MongoDB on a local server.
Steps to set this up on your own machine are linked here:
Get MongoDB installed: https://www.mongodb.com/
Import the dataset to a database/collection: https://www.mongodb.com/docs/guides/server/import/ 

A NOTE ON MEMORY: The actual query to extract the books from the database requests all books in English and pulls ~700k titles. However, due to memory constaints, 
the notebook only uses 20k rows of the dataset. It is recommended that any wish to increase the data size would be to batch the data and then run through the code. 

