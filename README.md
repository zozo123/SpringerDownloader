# SpringerDownloader

During the Corona (Covid-19) outbreak of 2020 many domains released some of their content for free use.
One of such domains was Springer site. It released 407 (389 at the current moment) free books in English.

Link: https://link.springer.com/search?showAll=false&package=mat-covid19_textbooks&facet-content-type=%22Book%22

We present here a short python script for downloading these free books. It is based on the following observation.

Consider an (example) url of the download page of one of the books:
  https://link.springer.com/book/10.1007/978-981-13-8759-3
It leads to download button of the pdf-file with the following path:
  https://link.springer.com/content/pdf/10.1007/978-981-13-8759-3.pdf
It also leads to the download button of the epub-file with the following path:
  https://link.springer.com/download/epub/10.1007/978-981-13-8759-3.epub
Considering other examples we detect the same structure of the paths.
We use this observation in our approach.

Note:
1. Our goal becomes much easier if you download the search results as csv-file (click on the down-arrow button in the upper right corner of the search results page). For your convinience we attach the file including information on all 407 books.
You can narrow down this list accordig to your needs.
2. Some of the authors' names are presented in their local language. Thus we use the following naming convention for the downloaded files "{book title} {DOI number}".
3. In the nearest future we will release two short python scripts (one for chars analysis and one for changing the authors' names so they will consist only of valid latin letters). The second script will be able to change all the downloaded books' names into conventional "{author} - {title}" filenames.
4. Not every book has its epub version, thus we use try-except handling in our code. (It is always a good practice to use exceptions handling to avoid crashes of the code in uncertain environment).

# Disclaimer
We emphasize, that this script (from our side) was written only as a programming exercise in python. We do not use it in any systematic manner, we do not suggest to use it before you become familiar with Springer's General Term of Use. We do not suggest to use it or any part of it on any content that was not defined as free content by the publisher.
