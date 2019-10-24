# stocksight Change Log

## [0.1-b.7] = 2019-10-23
### added
- check if running Python 3
- -U --upload - uploads sentiment to stocksight website (BETA) https://stocksight.diskoverspace.com/
- stocksight_token in config.py.sample, used for auth to upload to stocksight website
- tweet/news headline count/filtered/ratio log output
- --noelasticsearch cli arg for not adding new docs to Elasticsearch
- -s stock symbol cli arg (required arg)
- --overridetokensreq and --overridetokensignore cli args
- -a --addtokens cli arg to add nltk required tokens from config to keywords
### changed
- --newsheadlines no longer requires stock symbol, use -s to provide stock symbol
- nltk required tokens from config now do not automatically get added to keywords, use -a or --addtokens to add them
### fixed
- 'NoneType' object is not iterable Can't get sentiment from url caused by 400 Form Validation Errors text: This field is required traceback error when tweet with no text passed to sentiment_analysis

## [0.1-b.6] = 2019-07-15
### fixed
- "TypeError: sequence item 0: expected str instance, int found" traceback error when running with -f twitteruserids.txt

## [0.1-b.5] = 2019-01-11
### changed
- set encoding to utf-8 and checked for bytes when writing to twitteruserids.txt

## [0.1-b.4] = 2018-12-10
### fixed
- TypeError: can't concat str to bytes when writing to twitteruserids.txt

## [0.1-b.3] = 2018-11-23
### added
- requirements.txt for installing python requirements with pip
- config.py.sample has new setting for specifying elasticsearch host/ip, port, username and password, copy to your config file

## [0.1-b.2] = 2018-10-10
### added
- cli option -n --newsheadlines to fetch and analyze stock symbol headlines from yahoo finance website instead of twitter
- cli option --frequency to control how often news headlines are retrieved
- cli option --followlinks to follow any links in news headlines and scrape any relevant text on landing page
- additional mappings for newsheadline docs in elasticsearch indices
### changed
- code cleanup

## [0.1-b.1] = 2018-10-09
### note
- first release
