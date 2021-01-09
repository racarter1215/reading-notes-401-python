# List Comprehensions

## List comprehensions: they provide a concise way to create lists

### Parts: brackets containing an expression followed by a "for" clause, then zero or more for or if clauses

#### Will result in a new list resulting from evaluating the expression in the context of the for and if clauses which follow it.

#### Old Way Example:
new_list = []
for i in old_list:
    if filter(i):
        new_list.append(expressions(i))
        

#### New Way Example:
new_list = [expression(i) for i in old_list if filter(i)]

#### Basic syntax: [ expression for item in list if conditional ]

#### Equivalent expression: 

for item in list:
    if conditional:
        expression
        
#### What each part does:

##### new_list: new list (result).

##### expression(i): based on the variable used for each element in the old list.

##### for i in old_list: the word for followed by the variable name to use, followed by the word in the old list.

##### if filter(i): apply a filter with an If-statement.

##### Example List:
x = [i for i in range(10)]
print x

# This will give the output:
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

##### Example List Manipulation:

###### You can either use loops:
squares = []

for x in range(10):
    squares.append(x**2)
 
print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

###### Or you can use list comprehensions to get the same result:
squares = [x**2 for x in range(10)]

print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

##### Multiply List:
list1 = [3,4,5]
 
multiplied = [item*3 for item in list1] 
 
print multiplied 
[9,12,15]

##### Part of each item in array manipulation

listOfWords = ["this","is","a","list","of","words"]

items = [ word[0] for word in listOfWords ]

print items


