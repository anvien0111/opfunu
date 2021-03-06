# Optimization Function in Numpy (OpFuNu)
[![PyPI version](https://badge.fury.io/py/opfunu.svg)](https://badge.fury.io/py/opfunu)

## Installation

Install the [current PyPI release](https://pypi.python.org/pypi/opfunu):

```bash
pip install opfunu
```

Or install the development version from GitHub:

```bash
pip install git+https://github.com/thieunguyen5991/opfunu
```


## Example
+ All you need to do is: (Make sure your solution is a numpy 1-D array)
```python 
## For dimension_based

from opfunu.dimension_based.benchmark2d import Functions        # import 2-d benchmark functions
import numpy as np

solution2d = np.array([-0.1, 1.5])                              # Solution for 2-d benchmark
func2d = Functions()                                            # create an object

print(func2d._bartels_conn__(solution2d))                       # using function in above object
print(func2d._bird__(solution2d))

## For type_based (same as dimension_based)

from opfunu.type_based.multi_modal import Functions             # import 2-d benchmark functions
import numpy as np

## For CEC

from opfunu.cec.cec2014 import Functions                        # import cec2014 functions
import numpy as np

cec_sol = np.array([-0.1, 1.5])                              # Solution for 2-d benchmark
cec_func = Functions()                                            # create an object

print(cec_func.C1(cec_sol))                                  # using function in above object from C1, ..., C30
print(cec_func.C30(cec_sol))

...
```

### Publications
+ If you see my code and data useful and use it, please cites my works here
    + Nguyen, T., Nguyen, T., Nguyen, B. M., & Nguyen, G. (2019). Efficient Time-Series Forecasting Using Neural Network and Opposition-Based Coral Reefs Optimization. International Journal of Computational Intelligence Systems, 12(2), 1144-1161.
    
    + Nguyen, T., Tran, N., Nguyen, B. M., & Nguyen, G. (2018, November). A Resource Usage Prediction System Using Functional-Link and Genetic Algorithm Neural Network for Multivariate Cloud Metrics. In 2018 IEEE 11th Conference on Service-Oriented Computing and Applications (SOCA) (pp. 49-56). IEEE.

    + Nguyen, T., Nguyen, B. M., & Nguyen, G. (2019, April). Building Resource Auto-scaler with Functional-Link Neural Network and Adaptive Bacterial Foraging Optimization. In International Conference on Theory and Applications of Models of Computation (pp. 501-517). Springer, Cham.

+ This project related to my another projects which are "meta-heuristics" and "neural-network", check it here
    + https://github.com/thieunguyen5991/metaheuristics
    + https://github.com/chasebk

### Documentation 
```code 
1. dimension_based references
    1. http://benchmarkfcns.xyz/fcns
    2. https://en.wikipedia.org/wiki/Test_functions_for_optimization
    3. https://www.cs.unm.edu/~neal.holts/dga/benchmarkFunction/
    4. http://www.sfu.ca/~ssurjano/optimization.html

2. type_based
    A Literature Survey of Benchmark Functions For Global Optimization Problems (2013)

3. cec
    Problem Definitions and Evaluation Criteria for the CEC 2014 
Special Session and Competition on Single Objective Real-Parameter Numerical Optimization 

```
