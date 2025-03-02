# Project 2321: Probability
----



![1](2321_1.jpg)

## Resources

**Read or watch**:

* [Probability](https://en.wikipedia.org/wiki/Probability)
* [Basic Concepts](https://onlinestatbook.com/2/probability/basic.html)
* [Intro to probability 1: Basic notation](https://www.youtube.com/watch?v=TkU3BvDAOtQ)
* [Intro to probability 2: Independent and disjoint](https://www.youtube.com/watch?v=GnWHt9nqwBA)
* [Intro to Probability 3: General Addition Rule; Union; OR](https://www.youtube.com/watch?v=TyAaVGR4MrA)
* [Intro to Probability 4: General multiplication rule; Intersection; AND](https://www.youtube.com/watch?v=wB-ZG9bgPXY)
* [Permutations and Combinations](https://onlinestatbook.com/2/probability/permutations.html)
* [Probability distribution](https://en.wikipedia.org/wiki/Probability_distribution)
* [Probability Theory](https://medium.com/towards-data-science/probability-fundamentals-of-machine-learning-part-1-a156b4703e69)
* [Cumulative Distribution Functions](https://www.oreilly.com/library/view/think-stats-2nd/9781491907344/ch04.html)
* [Common Probability Distributions: The Data Scientist’s Crib Sheet](https://medium.com/@srowen/common-probability-distributions-347e6b945ce4)
* [NORMAL MODEL PART 1 — EMPIRICAL RULE](https://www.youtube.com/watch?v=xgolpGrAZWo&list=PLFGZup_HuWTtIs0Xbzt7vDoFrnZxN4VXT&index=22)
* [Normal Distribution](https://www.mathsisfun.com/data/standard-normal-distribution.html)
* [Variance](https://en.wikipedia.org/wiki/Variance)
* [Variance (Concept)](https://www.youtube.com/watch?v=2eP14USYwtg)
* [Binomial Distribution](https://onlinestatbook.com/2/probability/binomial.html)
* [Poisson Distribution](https://onlinestatbook.com/2/probability/poisson.html)
* [Hypergeometric Distribution](https://onlinestatbook.com/2/probability/hypergeometric.html)

**As references**:

* [numpy.random.poisson](https://docs.scipy.org/doc/numpy-1.14.0/reference/generated/numpy.random.poisson.html)
* [numpy.random.exponential](https://docs.scipy.org/doc/numpy-1.14.0/reference/generated/numpy.random.exponential.html)
* [numpy.random.normal](https://docs.scipy.org/doc/numpy-1.14.0/reference/generated/numpy.random.normal.html)
* [numpy.random.binomial](https://docs.scipy.org/doc/numpy-1.14.0/reference/generated/numpy.random.binomial.html)
* [erf](https://mathworld.wolfram.com/Erf.html)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What is probability?
* Basic probability notation
* What is independence? What is disjoint?
* What is a union? intersection?
* What are the general addition and multiplication rules?
* What is a probability distribution?
* What is a probability distribution function? probability mass function?
* What is a cumulative distribution function?
* What is a percentile?
* What is mean, standard deviation, and variance?
* Common probability distributions
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`python3`(version 3.9)
* All your files should end with a new line
* The first line of all your files should be exactly`#!/usr/bin/env python3`
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`pycodestyle`style (version 2.11.1)
* All your modules should have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions (inside and outside a class) should have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`and`python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* Unless otherwise noted, you are not allowed to import any module
* All your files must be executable
* The length of your files will be tested using`wc`
## Mathematical Approximations

For the following tasks, you will have to use various irrational numbers and functions. Since you are not able to import any libraries, please use the following approximations:

* *&Pi;*= 3.1415926536
* *e*= 2.7182818285
* ![1](2321_1.gif)
**Great!**You've completed the quiz successfully! Keep going!#### Question #0

What does the expression`P(A | B)`represent?

 * The probability of A and B

 * The probability of A or B

 * The probability of A and not B

 * The probability of A given B

#### Question #1

What does the expression`P(A &cap; B')`represent?

 * The probability of A and B

 * The probability of A or B

 * The probability of A and not B

 * The probability of A given B

#### Question #2

What does the expression`P(A &cap; B)`represent?

 * The probability of A and B

 * The probability of A or B

 * The probability of A and not B

 * The probability of A given B

#### Question #3

What does the expression`P(A &cup; B)`represent?

 * The probability of A and B

 * The probability of A or B

 * The probability of A and not B

 * The probability of A given B

#### Question #4

![1](2321_1.png)

The above image displays the normal distribution of male heights. What is the mode height?

 * 5'6"

 * 5'8"

 * 5'10"

 * 6’

 * 6'2"

#### Question #5

![2](2321_2.png)

The above image displays the normal distribution of male heights. What is the standard deviation?

 * 1"

 * 2"

 * 4"

 * 8"

#### Question #6

![3](2321_3.png)

The above image displays the normal distribution of male heights. What is the variance?

 * 4"

 * 8"

 * 16"

 * 64"

#### Question #7

![4](2321_4.png)

The above image displays the normal distribution of male heights. If a man is 6'6", what percentile would he be in?

 * 84th percentile

 * 95th percentile

 * 97.25th percentile

 * 99.7th percentile

#### Question #8

![2](2321_2.gif)

What type of distribution is displayed above?

 * Gaussian

 * Hypergeometric

 * Chi-Squared

 * Poisson

#### Question #9

![5](2321_5.png)

What type of distribution is displayed above?

 * Gaussian

 * Hypergeometric

 * Chi-Squared

 * Poisson

#### Question #10

What is the difference between a PDF and a PMF?

 * PDF is for discrete variables while PMF is for continuous variables

 * PDF is for continuous variables while PMF is for discrete variables

 * There is no difference

#### Question #11

For a given distribution, the value at the 50th percentile is always:

 * mean

 * median

 * mode

 * all of the above

#### Question #12

For a given distribution, the CDF(x) where x &isin; X:

 * The probability that X = x

 * The probability that X <= x

 * The percentile of x

 * The probability that X >= x


----
## Tasks
---
### 0. Initialize Poisson

Create a class <!--plain-NL-->`Poisson`<!--inline-NL--> that represents a poisson distribution:<!--plain-NL-->

- Class contructor `def __init__(self, data=None, lambtha=1.):`

`data` is a list of the data to be used to estimate the distribution
`lambtha` is the expected number of occurences in a given time frame
Sets the instance attribute `lambtha`

Saves `lambtha` as a float

If `data` is not given, (i.e. `None` (be careful: `not data` has not the same result as `data is None`)):


 Use the given `lambtha`
 If `lambtha` is not a positive value or equals to 0, raise a `ValueError` with the message `lambtha must be a positive value`

If `data` is given:


Calculate the `lambtha` of `data`
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- `data` is a list of the data to be used to estimate the distribution
- `lambtha` is the expected number of occurences in a given time frame
- Sets the instance attribute `lambtha`

Saves `lambtha` as a float
- Saves `lambtha` as a float
- If `data` is not given, (i.e. `None` (be careful: `not data` has not the same result as `data is None`)):


 Use the given `lambtha`
 If `lambtha` is not a positive value or equals to 0, raise a `ValueError` with the message `lambtha must be a positive value`
- Use the given `lambtha`
- If `lambtha` is not a positive value or equals to 0, raise a `ValueError` with the message `lambtha must be a positive value`
- If `data` is given:


Calculate the `lambtha` of `data`
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- Calculate the `lambtha` of `data`
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

- `data` is a list of the data to be used to estimate the distribution
- `lambtha` is the expected number of occurences in a given time frame
- Sets the instance attribute `lambtha`

Saves `lambtha` as a float
- Saves `lambtha` as a float
- If `data` is not given, (i.e. `None` (be careful: `not data` has not the same result as `data is None`)):


 Use the given `lambtha`
 If `lambtha` is not a positive value or equals to 0, raise a `ValueError` with the message `lambtha must be a positive value`
- Use the given `lambtha`
- If `lambtha` is not a positive value or equals to 0, raise a `ValueError` with the message `lambtha must be a positive value`
- If `data` is given:


Calculate the `lambtha` of `data`
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- Calculate the `lambtha` of `data`
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

- Saves `lambtha` as a float

- Use the given `lambtha`
- If `lambtha` is not a positive value or equals to 0, raise a `ValueError` with the message `lambtha must be a positive value`

- Calculate the `lambtha` of `data`
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

```
alexa@ubuntu-xenial:probability$ cat 0-main.py 
#!/usr/bin/env python3

import numpy as np
Poisson = __import__('poisson').Poisson

np.random.seed(0)
data = np.random.poisson(5., 100).tolist()
p1 = Poisson(data)
print('Lambtha:', p1.lambtha)

p2 = Poisson(lambtha=5)
print('Lambtha:', p2.lambtha)
alexa@ubuntu-xenial:probability$ ./0-main.py 
Lambtha: 4.84
Lambtha: 5.0
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `poisson.py`


---
### 1. Poisson PMF

Update the class <!--plain-NL-->`Poisson`<!--inline-NL-->:<!--plain-NL-->

- Instance method `def pmf(self, k):`

Calculates the value of the PMF for a given number of “successes”
`k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`

Returns the PMF value for `k`
- Calculates the value of the PMF for a given number of “successes”
- `k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`
- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`
- Returns the PMF value for `k`

- Calculates the value of the PMF for a given number of “successes”
- `k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`
- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`
- Returns the PMF value for `k`

- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`

```
alexa@ubuntu-xenial:probability$ cat 1-main.py 
#!/usr/bin/env python3

import numpy as np
Poisson = __import__('poisson').Poisson

np.random.seed(0)
data = np.random.poisson(5., 100).tolist()
p1 = Poisson(data)
print('P(9):', p1.pmf(9))

p2 = Poisson(lambtha=5)
print('P(9):', p2.pmf(9))
alexa@ubuntu-xenial:probability$ ./1-main.py 
P(9): 0.03175849616802446
P(9): 0.036265577412911795
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `poisson.py`


---
### 2. Poisson CDF

Update the class <!--plain-NL-->`Poisson`<!--inline-NL-->:<!--plain-NL-->

- Instance method `def cdf(self, k):`

Calculates the value of the CDF for a given number of “successes”
`k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`

Returns the CDF value for `k`
- Calculates the value of the CDF for a given number of “successes”
- `k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`
- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`
- Returns the CDF value for `k`

- Calculates the value of the CDF for a given number of “successes”
- `k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`
- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`
- Returns the CDF value for `k`

- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`

```
alexa@ubuntu-xenial:probability$ cat 2-main.py 
#!/usr/bin/env python3

import numpy as np
Poisson = __import__('poisson').Poisson

np.random.seed(0)
data = np.random.poisson(5., 100).tolist()
p1 = Poisson(data)
print('F(9):', p1.cdf(9))

p2 = Poisson(lambtha=5)
print('F(9):', p2.cdf(9))
alexa@ubuntu-xenial:probability$ ./2-main.py 
F(9): 0.9736102067423525
F(9): 0.9681719426208609
alexa@ubuntu-xenial:probability$ 

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `poisson.py`


---
### 3. Initialize Exponential

Create a class <!--plain-NL-->`Exponential`<!--inline-NL--> that represents an exponential distribution:<!--plain-NL-->

- Class contructor `def __init__(self, data=None, lambtha=1.):`

`data` is a list of the data to be used to estimate the distribution
`lambtha` is the expected number of occurences in a given time frame
Sets the instance attribute `lambtha`

Saves `lambtha` as a float

If `data` is not given (i.e. `None`):


Use the given `lambtha`
If `lambtha` is not a positive value, raise a `ValueError` with the message `lambtha must be a positive value`

If `data` is given:


Calculate the `lambtha` of `data`
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- `data` is a list of the data to be used to estimate the distribution
- `lambtha` is the expected number of occurences in a given time frame
- Sets the instance attribute `lambtha`

Saves `lambtha` as a float
- Saves `lambtha` as a float
- If `data` is not given (i.e. `None`):


Use the given `lambtha`
If `lambtha` is not a positive value, raise a `ValueError` with the message `lambtha must be a positive value`
- Use the given `lambtha`
- If `lambtha` is not a positive value, raise a `ValueError` with the message `lambtha must be a positive value`
- If `data` is given:


Calculate the `lambtha` of `data`
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- Calculate the `lambtha` of `data`
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

- `data` is a list of the data to be used to estimate the distribution
- `lambtha` is the expected number of occurences in a given time frame
- Sets the instance attribute `lambtha`

Saves `lambtha` as a float
- Saves `lambtha` as a float
- If `data` is not given (i.e. `None`):


Use the given `lambtha`
If `lambtha` is not a positive value, raise a `ValueError` with the message `lambtha must be a positive value`
- Use the given `lambtha`
- If `lambtha` is not a positive value, raise a `ValueError` with the message `lambtha must be a positive value`
- If `data` is given:


Calculate the `lambtha` of `data`
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- Calculate the `lambtha` of `data`
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

- Saves `lambtha` as a float

- Use the given `lambtha`
- If `lambtha` is not a positive value, raise a `ValueError` with the message `lambtha must be a positive value`

- Calculate the `lambtha` of `data`
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

```
alexa@ubuntu-xenial:probability$ cat 3-main.py 
#!/usr/bin/env python3

import numpy as np
Exponential = __import__('exponential').Exponential

np.random.seed(0)
data = np.random.exponential(0.5, 100).tolist()
e1 = Exponential(data)
print('Lambtha:', e1.lambtha)

e2 = Exponential(lambtha=2)
print('Lambtha:', e2.lambtha)
alexa@ubuntu-xenial:probability$ ./3-main.py 
Lambtha: 2.1771114730906937
Lambtha: 2.0
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `exponential.py`


---
### 4. Exponential PDF

Update the class <!--plain-NL-->`Exponential`<!--inline-NL-->:<!--plain-NL-->

- Instance method `def pdf(self, x):`

Calculates the value of the PDF for a given time period
`x` is the time period
Returns the PDF value for `x`
If `x` is out of range, return `0`
- Calculates the value of the PDF for a given time period
- `x` is the time period
- Returns the PDF value for `x`
- If `x` is out of range, return `0`

- Calculates the value of the PDF for a given time period
- `x` is the time period
- Returns the PDF value for `x`
- If `x` is out of range, return `0`

```
alexa@ubuntu-xenial:probability$ cat 4-main.py 
#!/usr/bin/env python3

import numpy as np
Exponential = __import__('exponential').Exponential

np.random.seed(0)
data = np.random.exponential(0.5, 100).tolist()
e1 = Exponential(data)
print('f(1):', e1.pdf(1))

e2 = Exponential(lambtha=2)
print('f(1):', e2.pdf(1))
alexa@ubuntu-xenial:probability$ ./4-main.py 
f(1): 0.24681591903431568
f(1): 0.2706705664650693
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `exponential.py`


---
### 5. Exponential CDF

Update the class <!--plain-NL-->`Exponential`<!--inline-NL-->:<!--plain-NL-->

- Instance method `def cdf(self, x):`

Calculates the value of the CDF for a given time period
`x` is the time period
Returns the CDF value for `x`
If `x` is out of range, return `0`
- Calculates the value of the CDF for a given time period
- `x` is the time period
- Returns the CDF value for `x`
- If `x` is out of range, return `0`

- Calculates the value of the CDF for a given time period
- `x` is the time period
- Returns the CDF value for `x`
- If `x` is out of range, return `0`

```
alexa@ubuntu-xenial:probability$ cat 5-main.py 
#!/usr/bin/env python3

import numpy as np
Exponential = __import__('exponential').Exponential

np.random.seed(0)
data = np.random.exponential(0.5, 100).tolist()
e1 = Exponential(data)
print('F(1):', e1.cdf(1))

e2 = Exponential(lambtha=2)
print('F(1):', e2.cdf(1))
alexa@ubuntu-xenial:probability$ ./5-main.py 
F(1): 0.886631473819791
F(1): 0.8646647167674654
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `exponential.py`


---
### 6. Initialize Normal

Create a class <!--plain-NL-->`Normal`<!--inline-NL--> that represents a normal distribution:<!--plain-NL-->

- Class contructor `def __init__(self, data=None, mean=0., stddev=1.):`

`data` is a list of the data to be used to estimate the distribution
`mean` is the mean of the distribution
`stddev` is the standard deviation of the distribution
Sets the instance attributes `mean` and `stddev`

Saves `mean` and `stddev` as floats

If `data` is not given (i.e. `None` (be careful: `not data` has not the same result as `data is None`))


Use the given `mean` and `stddev`
If `stddev` is not a positive value or equals to 0, raise a `ValueError` with the message `stddev must be a positive value`

If `data` is given:


Calculate the mean and standard deviation of `data`
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- `data` is a list of the data to be used to estimate the distribution
- `mean` is the mean of the distribution
- `stddev` is the standard deviation of the distribution
- Sets the instance attributes `mean` and `stddev`

Saves `mean` and `stddev` as floats
- Saves `mean` and `stddev` as floats
- If `data` is not given (i.e. `None` (be careful: `not data` has not the same result as `data is None`))


Use the given `mean` and `stddev`
If `stddev` is not a positive value or equals to 0, raise a `ValueError` with the message `stddev must be a positive value`
- Use the given `mean` and `stddev`
- If `stddev` is not a positive value or equals to 0, raise a `ValueError` with the message `stddev must be a positive value`
- If `data` is given:


Calculate the mean and standard deviation of `data`
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- Calculate the mean and standard deviation of `data`
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

- `data` is a list of the data to be used to estimate the distribution
- `mean` is the mean of the distribution
- `stddev` is the standard deviation of the distribution
- Sets the instance attributes `mean` and `stddev`

Saves `mean` and `stddev` as floats
- Saves `mean` and `stddev` as floats
- If `data` is not given (i.e. `None` (be careful: `not data` has not the same result as `data is None`))


Use the given `mean` and `stddev`
If `stddev` is not a positive value or equals to 0, raise a `ValueError` with the message `stddev must be a positive value`
- Use the given `mean` and `stddev`
- If `stddev` is not a positive value or equals to 0, raise a `ValueError` with the message `stddev must be a positive value`
- If `data` is given:


Calculate the mean and standard deviation of `data`
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- Calculate the mean and standard deviation of `data`
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

- Saves `mean` and `stddev` as floats

- Use the given `mean` and `stddev`
- If `stddev` is not a positive value or equals to 0, raise a `ValueError` with the message `stddev must be a positive value`

- Calculate the mean and standard deviation of `data`
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

```
alexa@ubuntu-xenial:probability$ cat 6-main.py 
#!/usr/bin/env python3

import numpy as np
Normal = __import__('normal').Normal

np.random.seed(0)
data = np.random.normal(70, 10, 100).tolist()
n1 = Normal(data)
print('Mean:', n1.mean, ', Stddev:', n1.stddev)

n2 = Normal(mean=70, stddev=10)
print('Mean:', n2.mean, ', Stddev:', n2.stddev)
alexa@ubuntu-xenial:probability$ ./6-main.py 
Mean: 70.59808015534485 , Stddev: 10.078822447165797
Mean: 70.0 , Stddev: 10.0
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `normal.py`


---
### 7. Normalize Normal

Update the class <!--plain-NL-->`Normal`<!--inline-NL-->:<!--plain-NL-->

- Instance method `def z_score(self, x):`

Calculates the z-score of a given x-value
`x` is the x-value
Returns the z-score of `x`
- Calculates the z-score of a given x-value
- `x` is the x-value
- Returns the z-score of `x`
- Instance method `def x_value(self, z):`

Calculates the x-value of a given z-score
`z` is the z-score
Returns the x-value of `z`
- Calculates the x-value of a given z-score
- `z` is the z-score
- Returns the x-value of `z`

- Calculates the z-score of a given x-value
- `x` is the x-value
- Returns the z-score of `x`

- Calculates the x-value of a given z-score
- `z` is the z-score
- Returns the x-value of `z`

```
alexa@ubuntu-xenial:probability$ cat 7-main.py 
#!/usr/bin/env python3

import numpy as np
Normal = __import__('normal').Normal

np.random.seed(0)
data = np.random.normal(70, 10, 100).tolist()
n1 = Normal(data)
print('Z(90):', n1.z_score(90))
print('X(2):', n1.x_value(2))

n2 = Normal(mean=70, stddev=10)
print()
print('Z(90):', n2.z_score(90))
print('X(2):', n2.x_value(2))
alexa@ubuntu-xenial:probability$ ./7-main.py 
Z(90): 1.9250185174272068
X(2): 90.75572504967644

Z(90): 2.0
X(2): 90.0
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `normal.py`


---
### 8. Normal PDF

Update the class <!--plain-NL-->`Normal`<!--inline-NL-->:<!--plain-NL-->

- Instance method `def pdf(self, x):`

Calculates the value of the PDF for a given x-value
`x` is the x-value
Returns the PDF value for `x`
- Calculates the value of the PDF for a given x-value
- `x` is the x-value
- Returns the PDF value for `x`

- Calculates the value of the PDF for a given x-value
- `x` is the x-value
- Returns the PDF value for `x`

```
alexa@ubuntu-xenial:probability$ cat 8-main.py 
#!/usr/bin/env python3

import numpy as np
Normal = __import__('normal').Normal

np.random.seed(0)
data = np.random.normal(70, 10, 100).tolist()
n1 = Normal(data)
print('PSI(90):', n1.pdf(90))

n2 = Normal(mean=70, stddev=10)
print('PSI(90):', n2.pdf(90))
alexa@ubuntu-xenial:probability$ ./8-main.py 
PSI(90): 0.006206096804434349
PSI(90): 0.005399096651147344
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `normal.py`


---
### 9. Normal CDF

Update the class <!--plain-NL-->`Normal`<!--inline-NL-->:<!--plain-NL-->

- Instance method `def cdf(self, x):`

Calculates the value of the CDF for a given x-value
`x` is the x-value
Returns the CDF value for `x`
- Calculates the value of the CDF for a given x-value
- `x` is the x-value
- Returns the CDF value for `x`

- Calculates the value of the CDF for a given x-value
- `x` is the x-value
- Returns the CDF value for `x`

```
alexa@ubuntu-xenial:probability$ cat 9-main.py 
#!/usr/bin/env python3

import numpy as np
Normal = __import__('normal').Normal

np.random.seed(0)
data = np.random.normal(70, 10, 100).tolist()
n1 = Normal(data)
print('PHI(90):', n1.cdf(90))

n2 = Normal(mean=70, stddev=10)
print('PHI(90):', n2.cdf(90))
alexa@ubuntu-xenial:probability$ ./9-main.py 
PHI(90): 0.9829020110852376
PHI(90): 0.9922398930659416
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `normal.py`


---
### 10. Initialize Binomial

Create a class <!--plain-NL-->`Binomial`<!--inline-NL--> that represents a binomial distribution:<!--plain-NL-->

- Class contructor `def __init__(self, data=None, n=1, p=0.5):`

`data` is a list of the data to be used to estimate the distribution
`n` is the number of Bernoulli trials
`p` is the probability of a “success”
Sets the instance attributes `n` and `p`

Saves `n` as an integer and `p` as a float

If `data` is not given (i.e. `None`)


Use the given `n` and `p`
If `n` is not a positive value, raise a `ValueError` with the message `n must be a positive value`
If `p` is not a valid probability, raise a `ValueError` with the message `p must be greater than 0 and less than 1`

If `data` is given:


Calculate `n` and `p` from `data`
Round `n` to the nearest integer (**rounded, not casting!** The difference is important: `int(3.7)` is not the same as `round(3.7)`)
*Hint: Calculate `p` first and then calculate `n`. Then recalculate `p`. Think about why you would want to do it this way?*
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- `data` is a list of the data to be used to estimate the distribution
- `n` is the number of Bernoulli trials
- `p` is the probability of a “success”
- Sets the instance attributes `n` and `p`

Saves `n` as an integer and `p` as a float
- Saves `n` as an integer and `p` as a float
- If `data` is not given (i.e. `None`)


Use the given `n` and `p`
If `n` is not a positive value, raise a `ValueError` with the message `n must be a positive value`
If `p` is not a valid probability, raise a `ValueError` with the message `p must be greater than 0 and less than 1`
- Use the given `n` and `p`
- If `n` is not a positive value, raise a `ValueError` with the message `n must be a positive value`
- If `p` is not a valid probability, raise a `ValueError` with the message `p must be greater than 0 and less than 1`
- If `data` is given:


Calculate `n` and `p` from `data`
Round `n` to the nearest integer (**rounded, not casting!** The difference is important: `int(3.7)` is not the same as `round(3.7)`)
*Hint: Calculate `p` first and then calculate `n`. Then recalculate `p`. Think about why you would want to do it this way?*
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- Calculate `n` and `p` from `data`
- Round `n` to the nearest integer (**rounded, not casting!** The difference is important: `int(3.7)` is not the same as `round(3.7)`)
- *Hint: Calculate `p` first and then calculate `n`. Then recalculate `p`. Think about why you would want to do it this way?*
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

- `data` is a list of the data to be used to estimate the distribution
- `n` is the number of Bernoulli trials
- `p` is the probability of a “success”
- Sets the instance attributes `n` and `p`

Saves `n` as an integer and `p` as a float
- Saves `n` as an integer and `p` as a float
- If `data` is not given (i.e. `None`)


Use the given `n` and `p`
If `n` is not a positive value, raise a `ValueError` with the message `n must be a positive value`
If `p` is not a valid probability, raise a `ValueError` with the message `p must be greater than 0 and less than 1`
- Use the given `n` and `p`
- If `n` is not a positive value, raise a `ValueError` with the message `n must be a positive value`
- If `p` is not a valid probability, raise a `ValueError` with the message `p must be greater than 0 and less than 1`
- If `data` is given:


Calculate `n` and `p` from `data`
Round `n` to the nearest integer (**rounded, not casting!** The difference is important: `int(3.7)` is not the same as `round(3.7)`)
*Hint: Calculate `p` first and then calculate `n`. Then recalculate `p`. Think about why you would want to do it this way?*
If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`
- Calculate `n` and `p` from `data`
- Round `n` to the nearest integer (**rounded, not casting!** The difference is important: `int(3.7)` is not the same as `round(3.7)`)
- *Hint: Calculate `p` first and then calculate `n`. Then recalculate `p`. Think about why you would want to do it this way?*
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

- Saves `n` as an integer and `p` as a float

- Use the given `n` and `p`
- If `n` is not a positive value, raise a `ValueError` with the message `n must be a positive value`
- If `p` is not a valid probability, raise a `ValueError` with the message `p must be greater than 0 and less than 1`

- Calculate `n` and `p` from `data`
- Round `n` to the nearest integer (**rounded, not casting!** The difference is important: `int(3.7)` is not the same as `round(3.7)`)
- *Hint: Calculate `p` first and then calculate `n`. Then recalculate `p`. Think about why you would want to do it this way?*
- If `data` is not a `list`, raise a `TypeError` with the message `data must be a list`
- If `data` does not contain at least two data points, raise a `ValueError` with the message `data must contain multiple values`

```
alexa@ubuntu-xenial:probability$ cat 10-main.py 
#!/usr/bin/env python3

import numpy as np
Binomial = __import__('binomial').Binomial

np.random.seed(0)
data = np.random.binomial(50, 0.6, 100).tolist()
b1 = Binomial(data)
print('n:', b1.n, "p:", b1.p)

b2 = Binomial(n=50, p=0.6)
print('n:', b2.n, "p:", b2.p)
alexa@ubuntu-xenial:probability$ ./10-main.py 
n: 50 p: 0.606
n: 50 p: 0.6
alexa@ubuntu-xenial:probability$ 

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `binomial.py`


---
### 11. Binomial PMF

Update the class <!--plain-NL-->`Binomial`<!--inline-NL-->:<!--plain-NL-->

- Instance method `def pmf(self, k):`

Calculates the value of the PMF for a given number of “successes”
`k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`

Returns the PMF value for `k`
- Calculates the value of the PMF for a given number of “successes”
- `k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`
- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`
- Returns the PMF value for `k`

- Calculates the value of the PMF for a given number of “successes”
- `k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`
- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`
- Returns the PMF value for `k`

- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`

```
alexa@ubuntu-xenial:probability$ cat 11-main.py 
#!/usr/bin/env python3

import numpy as np
Binomial = __import__('binomial').Binomial

np.random.seed(0)
data = np.random.binomial(50, 0.6, 100).tolist()
b1 = Binomial(data)
print('P(30):', b1.pmf(30))

b2 = Binomial(n=50, p=0.6)
print('P(30):', b2.pmf(30))
alexa@ubuntu-xenial:probability$ ./11-main.py 
P(30): 0.11412829839570347
P(30): 0.114558552829524
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `binomial.py`


---
### 12. Binomial CDF

Update the class <!--plain-NL-->`Binomial`<!--inline-NL-->:<!--plain-NL-->

- Instance method `def cdf(self, k):`

Calculates the value of the CDF for a given number of “successes”
`k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`

Returns the CDF value for `k`
*Hint: use the `pmf` method*
- Calculates the value of the CDF for a given number of “successes”
- `k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`
- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`
- Returns the CDF value for `k`
- *Hint: use the `pmf` method*

- Calculates the value of the CDF for a given number of “successes”
- `k` is the number of “successes”


If `k` is not an integer, convert it to an integer
If `k` is out of range, return `0`
- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`
- Returns the CDF value for `k`
- *Hint: use the `pmf` method*

- If `k` is not an integer, convert it to an integer
- If `k` is out of range, return `0`

```
alexa@ubuntu-xenial:probability$ cat 12-main.py 
#!/usr/bin/env python3

import numpy as np
Binomial = __import__('binomial').Binomial

np.random.seed(0)
data = np.random.binomial(50, 0.6, 100).tolist()
b1 = Binomial(data)
print('F(30):', b1.cdf(30))

b2 = Binomial(n=50, p=0.6)
print('F(30):', b2.cdf(30))
alexa@ubuntu-xenial:probability$ ./12-main.py 
F(30): 0.5189392017296368
F(30): 0.5535236207894576
alexa@ubuntu-xenial:probability$

```

**Repo:**

- GitHub repository: `atlas-machine_learning`
- Directory: `math/probability`
- File: `binomial.py`