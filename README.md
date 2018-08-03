# epub
An experiment on creating a eBook in epub format from HTML files.

# Prepare the document
## Copy 10 .html files into a folder name 00
>  00/

>    E00001.html

>    ...

>    E00010.html

## Rename them to .xhtml on Ubuntu 16.04LTS:
>  rename 's/.html/.xhtml/' E*

## Updates the .xhtml files
* Update the begining of the file to make it look like this:

>  &lt;link rel="stylesheet" type="text/css" href="../css/doe.css" /&gt;

>  &lt;?xml version="1.0" encoding="UTF-8"?&gt;

>  &lt;html xml:lang="en" xmlns="http://www.w3.org/1999/xhtml"&gt;

>  &lt;head&gt;

>  &lt;link rel="stylesheet" type="text/css" href="../css/doe.css" /&gt;

>  &lt;title&gt; ... &lt;/title&gt;

>  &lt;/head&gt;

* Replace the named entities to numbered entities
>  perl -pi -e "s/&amp;eth;/&amp;#240;/g" E*.xhtml
