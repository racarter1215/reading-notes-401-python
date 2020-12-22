# What is Risk Analysis in Software Testing and how to perform it?

## Risk: The probability of any unwanted incident 

### Why use Risk Analysis?

### at the beginning of a project, it highlights the potential problem areas.

### Example Risks:
#### Use of new hardware
#### Use of new technology
#### Use of new automation tool
#### The sequence of code
#### Availability of test resources for the application

### Risk Identification Examples:
#### Business Risks
#### Software Risks
#### Testing Risks
#### Premature Release Risks

### Perspectives of Risk Assessment:
#### Effect
#### Cause
#### Likelihood

# How to use the Random Module in Python

## Randint example:
import random
print random.randint(0, 5)

### Random example:
import random
random.random() * 100

### Choice example:
random.choice( ['red', 'black', 'green'] ).

import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)

### Shuffle example:
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
Output:
##### print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]
##### of course your results will vary

### Randrange example:
random.randrange(start, stop[, step])
import random
for i in range(3):
    print random.randrange(0, 101, 5)

### Coin flip code example:
import random
import itertools

outcomes = { 'heads':0,
             'tails':0,
             }
sides = outcomes.keys()

for i in range(10000):
    outcomes[ random.choice(sides) ] += 1

print 'Heads:', outcomes['heads']
print 'Tails:', outcomes['tails']

$ python random_choice.py

Heads: 4984
Tails: 5016


