# CeneoScraperS11
## Stage 1 - extraction of all components for single opinion 
1. Extraction of a single web page content
2. Analisys of a single opinion structure 
|Component|CSS selector|Variable name|Data type|
|---------|------------|-------------|---------|
|Opinion|div.user-post_card|opinion||
|Opinion id|["data-entry-id"]|opinion_id|str|
|Author|span.user-post__author-name|author|str|
|Recommendation|span.user-post__author-recomendation > em|recommendation|bool|
|Stars rating|span.user-post__score-count|stars|float|
|Content|div.user-post__text|content||
|Advantages|div.review-feature__col:has(> div[class$="positives"]) > div.review-feature__item|pros|list (str)|
|Disadvantages|div.review-feature__col:has(> div[class$="negatives"]) > div.review-feature__item|cons|list(str)|
|Verification|div.review-pz|verified|bool|
|Post date|span.user-post__published > time:nth-child(1)["datetime"]|post_date|str|
|Purchase date|span.user-post__published > time:nth-child(2)["datetime"]|purchase_date|str|
|Usefulness count|span[id^="votes-yes"]|usefulness|int|
|Uselessness count|span[id^="votes-no"]|uselessness|int|
3. Extraction of single opinion components
4. Transformation of extracted data to given data types

## Stage 2 - extraction of all opinions from single page
1. Definition of a dictionary to store all of the opinion's components
2. Definition of a list to store dictionaries with opinions
3. Implementation of loop traversing thorugh all opinions from a single page

## Stage 3 - extraction of all opinions from single product
1. Implementation of loop traversing through consecutve pages with opinions
2. Loading extracted opinions to .json file
3. Parameterization of a product id 

## Stage 4 - code refactoring
