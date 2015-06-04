# PDF Structure and Syntactic Analysis for Metadata Extraction and Tagging #

PDFSSA4MET attempts to provide metadata extraction and tagging based on
structural and syntactic analysis of content in XML.

## Capabilities ##
Given PDFs that conform to a fairly conventional structure (e.g. scholarly works), attempts to extract and tag:
  * headings
    * title
    * author
    * chapter / section headings
  * references
    * title
    * volume
    * page numbers
    * cited publications and URLs
  * suggested social tags

Headings are identified by looking for text that deviates from the norm in terms of size, colour, or weight (bold).

References are identified by looking for patterns in the "References" section. Elements making up each reference are also identified by pattern matching.

Titles, Authors, Headings, References and the component elements are tagged with quick and dirty XML tags.

Scripts will have varying success between different PDFs, but will hopefully become more consistent and reliable with additional testing. If you want to contribute to improving the regexes please get in touch.

## Dependencies ##
  * PDF to XML conversion by binary [available from sourceforge](http://sourceforge.net/projects/pdf2xml/)
  * [Python 2.6+](http://www.python.org)
    * lxml
    * rdflib

## Download ##
Source code available as gzipped TAR archive and via Subversion.

## Usage ##
The following scripts can be used directly to output results to STDOUT:
  * pdf2xml.py
  * headings.py
  * references.py
  * socialtags.py

Help, options and arguments for each are available using -h or --help option
e.g.
```
python references.py --help
```