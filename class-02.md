# In Tests We Trust — TDD with Python

### Unit tests: Bits of code utilized to exercise the input/output and overall behaviour of code.

### Sample Test:
def test_should_return_female_when_the_name_is_from_female_gender():
    detector = GenderDetector()
    expected_gender = detector.run(‘Ana’)
    assert expected_gender == ‘female’
    
### Three parts of test: Arrange, Act, Assert

### More samples:
mymodule/
 — module.py
 — another_folder/
 — — another_module.py
tests/
 — test_module.py
 — another_folder/
 — — test_another_module.py
 

### The Cycle
#### Three Parts: Write unit test, write feature, refactor

## Recursion

### Recursion: The process in which a function calls itself

### This type of function is good for tree traversals, either Inorder, Preorder, or Postorder

### Example:
approach(1) – Simply adding one by one

f(n) = 1 + 2 + 3 +……..+ n

approach(2) – Recursive adding 

f(n) = 1                  n=1

f(n) = n + f(n-1)    n>1

### In recursion, the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems. 

### Example:
int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}

### Stack overflow errors can occur if your code gets stuck in an infinite recursion loop

### Direct and Indirect Recursion Examples:
// An example of direct recursion
void directRecFun()
{
    // Some code....

    directRecFun();

    // Some code...
}

// An example of indirect recursion
void indirectRecFun1()
{
    // Some code...

    indirectRecFun2();

    // Some code...
}
void indirectRecFun2()
{
    // Some code...

    indirectRecFun1();

    // Some code...
}

