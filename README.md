## Overview

In order to make AWS lambda as one of totuslink's NLP operation plaform, we need numpy, scikit-learn and pandas, but AWS lambda has memory hard limit 50 MB(zipped file). It's very hard to compress the file we need in such small package, but now we can use lambda-layer to help us compensate this limit, AWS had already maintenanced a scikit-learn lambda-layer which have scikit-learn and numpy. What we need to do is to build a pandas-layer, combine these two together to achieve our goal.

