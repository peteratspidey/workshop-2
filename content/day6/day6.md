#control structures in python 
## conditional (if,elif and else)
> this is a conditional loop where if one condition is not satisfied then move to the second condition and further condtions until first condition is satisfied

if condition == true:
  run the code body and dont move the code ahead
  print()
if condition != true:
run the elif condition:
if elif condition is == true
    run the code body and dont move ahead
if elif != true:
run the else condition
if else == true:
  run the code body and break the loop
if else != true:
  break

## loop (iteration)
### while
> repeat until condition is false

### for
> repeat untill given fix no of times
> faster than the while+if loop


## jump statements ( They help you exit, skip, or pause execution.)
### continue
>skip curren iteration , continue
> runs the iteration continously but only skip the condition with continue 

### break 
> exit loop early
> stops the iteration immediately after a condition and doesnt move along further

### pass
>Placeholder (does nothing)
> no error no output just hold the place for the condition and prevents from error
> use it for error handling

### try and accept( exception handling)
try:
    condition
except:
    body
> use to identifying the error and show is via except blocks
> there are so many types of error that can b use under try and except ( all listed in the error.md file)

***common use for handling any error***
try:
    # risky code
    x = int("abc")
except Exception as e:
    print("Error happened:", e)
> this will print the except block when find any error in the try block
