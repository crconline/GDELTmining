# GDELT Project Mining

<div style="text-align:center"><img src ="https://hadoopi.files.wordpress.com/2014/09/screen-shot-2014-09-24-at-20-55-34.png" width="400" /></div>

This project contains several python scripts developed to mine the GDELT project in search of a keyword in a URL.

1. The **GDELTmining.py** script searches GDELT project database by using keywords introduced as parameters from input device. It generates a directory **CSVfiles** containing the retrieved files which URL matches the keywords. Inside such directory, all web sites generated that day are retrieved in a zipped file, which is unzipped and the URL line is saved, then the URL's web site is retrieved in full text and saved into a subdirectory **TXTfiles**. The script also generates a log file containing statistics **URLstats.txt**.

2. The **authlistgen.py** script generates a list of authors by complete name taken from the database of authors generated with Web of Science utility. The list of edited names is saved in the generated file **authorslist.csv**.

3. The script **minefiles.py** is the one in charge of retrieving all matches between the authors' names and full text of each one of the files in the subdirectory **TXTitems**. It generates a report file **report.csv**.

4. Statistics of the GDELT data mining are generated with the script **uniqueauth.py**, which embed three functions to generate: a list of unique authors saved in the generated file **uniqueauthors.csv**; all sites that cite an author from the list, this is saved in the **sitelistingauthors.csv**; and a list of counted authors and the URLs citing them, this is saved in the generated file **report.csv**.



