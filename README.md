## Overview

In order to make AWS lambda as one of totuslink's NLP operation plaform, we need numpy, scikit-learn and pandas, but AWS lambda has memory hard limit 50 MB(zipped file). It's very hard to compress the file we need in such small package, but now we can use lambda-layer to help us compensate this limit, AWS had already maintenanced a scikit-learn lambda-layer which have scikit-learn and numpy. What we need to do is to build a pandas-layer, combine these two together to achieve our goal.

## Usage

### setup authority

```
    chmod +x get_layer_packages.sh
```

### get into file and zip it

```
    ./get_layer_packages.sh
```

## Caution
1. the file structure should be (take pillow package for example) 

pillow.zip
│ python/PIL
└ python/Pillow-5.3.0.dist-info
