# Data Loader

Python utility to extract metadata from OpenSlide images and post them to a RESTful interface

Installation:
* Tested on python 3.5.0.
* `pip install -r requirements.txt`

Make sure you have `LD_LIBRARY_PATH` set up 

### Usage:
`python dataLoader.py -i <inputCSVFile> -o <RESTinterface> -a <API key>`


#### Input.csv
This is the format of input.csv

```
Id, study_id, File
test1,default,/data/images/CMU-1.svs
test2,default,/data/images/CMU-2.svs

```

where 
* `Id` is the `case_id` of the image
* `study_id` is the `study_id`
* `File` is the file location on disk. 

### Issues
`ImportError: libopenjp2.so.7: cannot open shared object file.`

Run

`export LD_LIBRARY_PATH=/usr/local/lib`
to fix this.

