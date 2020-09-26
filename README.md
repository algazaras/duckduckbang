# Meta search tool builder

This script builds the html pages for a little meta-search tool;

The resulting meta-search tool [in action](https://mosermichael.github.io/duckduckbang/html/main.html) that makes use of the duckduckgo [bang!](https://duckduckgo.com/bang) search commands.

You can select a duckduckgo  bang! search operator, the operator then appears in the seach input box, where you can add your query; A search query is sent to duckduckgo that includes the selected bang! operator, once you press enter press the Go! button (or enter ; duckducko then redirects the query to a search engine specified by the operator.

A web search on duckduckgo that includes a bang! search command is redirected to a specialized search engine (the most famous bang operator is g! - a web search is redirected to google search if the term g! is added to the query text); now duckduckgo maintains a directory of these bang! search commands, each of these commands stands for a different search engine that takes over the web search.

The meta-search tool has the advantage of having all duckduckgo bang! search commands in one page, it uses the same catalog of operators as duckduckgo. I think having all bang! operators on one page makes it easier to use the feature.

The page is kept up to date by a nightly build process (runs courtesy of [github workflows/actions](https://docs.github.com/en/free-pro-team@latest/actions/learn-github-actions) ) Any new bang! operator should therefore appear in the search tool.

# Motivation for the search tool 

Lately I have been increasingly using specialised search engines; for example when searching for code examples it is possible to find quite a lot with [github search](https://github.com/search/advanced) (the search operators are explained [here](https://docs.github.com/en/free-pro-team@latest/github/searching-for-information-on-github/searching-code) and [here](https://docs.github.com/en/github/searching-for-information-on-github/understanding-the-search-syntax). I have not been able to get the same quality results in any of the big search engines.

Now general purpose search engines like [google](https://google.com), [bing](https://bing.com) and [yandex](https://yandex.com/) have a hard time to give reasonable answers to each and every search request. Google has a hard job: it has identify the intent of your query and give you the stuff that is relevant to your query - they also have to be good for a very wide range of individuals.

Specialized search engines have it much easier - they don't have to work hard to determine the intent of the query, as they are focused on a particular domain.  Also they may have a more focused and sometimes deeper index on a particular domain; You might consider using a specialized search engine if you fail to find the stuff with google or bing. With duckduckgo you get this huge classification with the bang! search operator (that's where this project comes in). 

These specialized search engines will also tend to respect your privacy, more than the big players do; specialized search engines might not have the resources to do much snooping anyway (this might not always be the case, depending on affiliation, etc. etc.)

# Script that builds the page

The [build-cats.py](https://github.com/MoserMichael/duckduckbang/blob/master/build-cats.py) script that generates the search page works as follows: 

1. It loads the following url [https://duckduckgo.com/bang.js](https://duckduckgo.com/bang.js) this gives a json file that contains an entry for each bang! search operator, and the classification of the operator in the official [bang page](https://duckduckgo.com/bang).
2. Builds the category/subcategory breakup that is used to display the [bang page](https://duckduckgo.com/bang).  
3. Formats an html page that contains all of the !bang operators into one page (maintain categories displayed in the official bang page)

The tool utilizes [duckduck go bang! operators](https://duckduckgo.com/bang)

# Today i learned

The abbreviation of Categories is cat; [here](https://writingexplained.org/english-abbreviations/category)
Are cats capable of categorization? No idea, I like them. 




