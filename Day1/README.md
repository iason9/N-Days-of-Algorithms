# Day 1
## Recursive methods
Recursive methods unlike iterative methods which are based on loops and in which they are step by step , are easy to write but in fact more complex to get the right approche and actually write them, indeed you will have to think about two key factors to create recursive functions, these keys are : the last value and the edge cases.

To understand recursive methods we have to compare it to the iterative methods, the iterative methods are based into a logic of step by step in which the first step begins from the start and then using its result go through the second and third using each time the result of the previous one until we get to the very end and get finlay the solution.
for example the calculation of X^n :
- we start by X*X 
  - lets say this result is : Y
- second step is Y * X  
  - lets say this result is : Z
- third step is Z * X
  - lets say this result is : Z

- And we continue until N times, you do see that we are using each time the previous result.

With recursive methods we work backwards by using the result of the last step and then going up to the very first step, we use the result of the last step because it's the only value we know.
we use a recursive function that calls itself, this function doesn't calculate anything it just specifies how to do the calculations in each call of the function, it is only at the last call of the function that the script knows the value that is needed, when it does, everything start to work backwards indeed all the previous function calls that were stacking up start to be called one by one. (it goes deep until it hits the final value and then ascend to the top to finally get the result).

we need to specify the final result otherwise the calls will never end and we will have an infinite recursive function.

again we need to know two things : the final value of the recursion and how the function is written because a recursive function is very elegant but needs to be well thought out, it is in the same time simple and complex but very powerful.

- Example of recursive function

```python
def power(x,N):
    # when we are at the final function call the if is true (N==0)
    if N == 0:
        result = 1.0
    else:
        result = x*power(x, N-1)

    # when we are at the final function call (N==0) this is returned 
    # also when all the function calls are completed this is returned as the final result
    return result

```
