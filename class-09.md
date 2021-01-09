# Enriching Your Python Classes With Dunder (Magic, Special) Methods

## Dunder methods:  let you emulate the behavior of built-in types.

### Example:
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
To fix this, you can add a __len__ dunder method to your class:

class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42

### You can also slice by using: __getitem__ obj[start:stop]

#### Python Data Model: It's like a powerful API you can interface with by implementing one or more dunder methods. 

#### __init__ example:
class Account:
    """A simple account class"""

    def __init__(self, owner, amount=0):
        """
        This is the constructor that lets us create
        objects from this class
        """
        self.owner = owner
        self.amount = amount
        self._transactions = []
        
#### __str__, __repr__ examples:
###### __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

###### __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

class Account:

    def __repr__(self):
        return 'Account({!r}, {!r})'.format(self.owner, self.amount)

    def __str__(self):
        return 'Account of {} with starting amount: {}'.format(
            self.owner, self.amount)

#### __len__, __getitem__, __reversed__ examples:
def add_transaction(self, amount):
    if not isinstance(amount, int):
        raise ValueError('please use int for amount')
    self._transactions.append(amount)

@property
def balance(self):
    return self.amount + sum(self._transactions)
Let’s do some deposits and withdrawals on the account:

>>> acc = Account('bob', 10)

>>> acc.add_transaction(20)
>>> acc.add_transaction(-10)
>>> acc.add_transaction(50)
>>> acc.add_transaction(-20)
>>> acc.add_transaction(30)

>>> acc.balance
80

class Account:
    # ... (see above)

    def __len__(self):
        return len(self._transactions)

    def __getitem__(self, position):
        return self._transactions[position]
Now the previous statements work:

>>> len(acc)
5

>>> for t in acc:
...    print(t)
20
-10
50
-20
30

>>> acc[1]
-10


# Basic Statistics in Python — Probability

## Probablility: what is the chance of an event happening?
## Event: some outcome of interest.

### Example coin flip:
import random
def coin_trial():
heads = 0
for i in range(100):
    if random.random() <= 0.5:
        heads +=1
    return heads
def simulate(n):
    trials = []
    for i in range(n):
        trials.append(coin_trial())
    return(sum(trials)/n)
simulate(10)
>>> 5.4
simulate(100)
>>> 4.83
simulate(1000)
>>> 5.055
simulate(1000000)
>>> 4.999781

#### Wine comparison example:
###### Extract the Tokaji scores
tokaji = []
non_tokaji = []
for wine in wines:
    if points != '':
        points = wine[4]
    if wine[9] == "Tokaji":
    tokaji.append(float(points))
    else:
        non_tokaji.append(points)
###### Extract the Lambrusco scores
lambrusco = []
non_lambrusco = []
for wine in wines:
    if points != '':
        points = wine[4]
    if wine[9] == "Lambrusco":
        lambrusco.append(float(points))
    else:
        non_lambrusco.append(float(points))
        
#### 
