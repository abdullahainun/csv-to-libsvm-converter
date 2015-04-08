Scripts to convert csv files to libsvm format for machine learning operations 
======
modified from __phraug__ by __zygmuntz__
-----------------

This is a first attempt at improving the csv2libsvm script for converting csv data files to libsvm format. The latter is commonly used for machine learning (e.g. MLLIB).

A linux shell script version of the script is also in development.

Additions to original csv2libsvm
-----------------
* returning result to STDOUT instead of output file
` csv2libsvm.py <input file> stdout <label index> <skip headers> <convert string classes> <output dict>`

* allowing the use of last column as label/class 
` csv2libsvm.py <input file> <output file> last <skip headers> <convert string classes> <output dict>`

* introducing a string classes conversion function for non-numeric classes
` csv2libsvm.py <input file> <output file> last <skip headers> convert_string <output dict>`
_note that output dict will show the mapping between your non-numeric classes and the numeric classes they are mapped to_


Format conversion
-----------------

`csv2libsvm.py <input file> <output file> [<label index = 0>] [<skip headers = 0>]`

Convert CSV to LIBSVM format. If there are no labels in the input file, specify _label index_ = -1. If there are headers in the input file, specify _skip headers_ = 1.

