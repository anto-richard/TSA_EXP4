# Ex.No:04   FIT ARMA MODEL FOR TIME SERIES...

# Date: 23/03/24

### AIM :

To implement ARMA model in python.

### ALGORITHM :

#### Step 1 :

Import necessary libraries.

#### Step 2 :

Set up matplotlib settings for figure size.

#### Step 3 :

Define an ARMA(1,1) process with coefficients ar1 and ma1, and generate a sample of 1000 data points using the ArmaProcess class. Plot the generated time series and set the title and x- axis limits.

#### Step 4 :

Display the autocorrelation and partial autocorrelation plots for the ARMA(1,1) process using plot_acf and plot_pacf.

#### Step 5 : 

Define an ARMA(2,2) process with coefficients ar2 and ma2, and generate a sample of 10000 data points using the ArmaProcess class. Plot the generated time series and set the title and x-axis limits.

#### Step 6 :

Display the autocorrelation and partial autocorrelation plots for the ARMA(2,2) process using plot_acf and plot_pacf.

### PROGRAM :

```python

from pandas import read_csv
from pandas import datetime
from matplotlib import pyplot
from pandas.plotting import autocorrelation_plot
from pandas import DataFrame
from statsmodels.tsa.arima_model import ARIMA
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
from statsmodels.tsa.arima_process import ArmaProcess
import matplotlib.pyplot as plt
import numpy as np
import warnings
warnings.filterwarnings('ignore')
import matplotlib.pyplot as plt
import numpy as np

plt.rcParams['figure.figsize'] = [10, 7.5]

ar1 = np.array([1,0.33])
ma1 = np.array([1,0.9])
ARMA_1 = ArmaProcess(ar1,ma1).generate_sample(nsample = 1000)
plt.plot(ARMA_1)
plt.title('Simulated ARMA(1,1) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_1)
plot_pacf(ARMA_1)
ar2 = np.array([1, 0.33, 0.5])
ma2 = np.array([1, 0.9, 0.3])
ARMA_2 = ArmaProcess(ar2, ma2).generate_sample(nsample=10000)
plt.plot(ARMA_2)
plt.title('Simulated ARMA(2,2) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_2)
plot_pacf(ARMA_2)

```

### OUTPUT :

#### SIMULATED ARMA(1,1) PROCESS :

![img1](https://github.com/anto-richard/TSA_EXP4/assets/93427534/cc8bd67b-6872-4986-a714-b088f29b9f5a)

#### Partial Autocorrelation :

![img2](https://github.com/anto-richard/TSA_EXP4/assets/93427534/3ae2f06e-aaa9-4f14-98e7-096fed38fb8a)

#### Autocorrelation :

![img3](https://github.com/anto-richard/TSA_EXP4/assets/93427534/1796dd43-d73b-4f28-b625-bbdb3ddd9819)

#### SIMULATED ARMA(2,2) PROCESS :

![img4](https://github.com/anto-richard/TSA_EXP4/assets/93427534/2c71bf88-27a5-4eea-aa7e-010c6cf16630)

#### Partial Autocorrelation :

![img5](https://github.com/anto-richard/TSA_EXP4/assets/93427534/f862f420-0e07-4227-b46a-94405235410d)

#### Autocorrelation :

![img6](https://github.com/anto-richard/TSA_EXP4/assets/93427534/df96442c-d141-4580-aea7-4c99308582b0)

### RESULT :

Thus, a python program is created to fit the ARMA Model successfully.

