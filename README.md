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
case_id, filename, extra_id
image1, /data/images/17035673.svs, test1
image2, /data/images/CMU-2.svs, test2
```

where the following 2 are *mandatory* in the CSV:
* `case_id` is the unique identifier for the image
* `filename` is the file location on disk. 

any additional fields like `extra_id` are appended to the final metadata JSON.



### Issues
`ImportError: libopenjp2.so.7: cannot open shared object file.`

Run

`export LD_LIBRARY_PATH=/usr/local/lib`
to fix this.

