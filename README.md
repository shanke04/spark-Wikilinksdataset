# spark-Wikilinksdataset
(1question)- For each record in wikilinks , extract The URL of the page ((annotated by “URL) and all the urls of
the websites that this page links to (annotated by MENTION). That means, you want to create an
RDD of the form (<URL1>,< URL2>) where URL1 is the URL of the page and URL2 is the URL of a
page mentioned /linked to by URL1.
For example, if have the following record in wikilinks:
URL ftp://217.219.170.14/Computer%20Group/sattari/word
MENTION vacuum tube 421 http://en.wikipedia.org/wiki/Vacuum_tube
MENTION vacuum tubes 10838 http://en.wikipedia.org/wiki/Vacuum_tube
Then you want to create a pair rdd with the following elements:
(ftp://217.219.170.14/Computer%20Group/sattari/word,
http://en.wikipedia.org/wiki/Vacuum_tube)
(ftp://217.219.170.14/Computer%20Group/sattari/word,
http://en.wikipedia.org/wiki/Vacuum_tube)
(2question)- Find the number of times each URL has been mentioned by another URL and find 10 most
frequently mentioned URLS.
(3question)- Find the number of symmetric URL pairs <URL1,URL2> such that URL1 mentions URL2 and URL2
mentions URL1 . (Is there any such symmetric pairs in wikilinks?)
