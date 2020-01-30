# week 02 / lecture 9

repl by Priyesh -- https://repl.it/repls/ElasticSilverHypertalk (please copy for reference later)



## while loop

* used for indefinite iternations, when you do not know the exit condition

* regular increment, in each run of loop 

  ```python
  age = 17
  while (age<18):
    print("you are illegal, access denied")
    age+=1
  # while is most useful when increments are not regular
  print("chill")
  ```

* exit condition -- to make loop continue to run , we need to iterate e



## break

* real life example of break statement -- if water runs out, bucket may or may not fill depending on time of day when water comes

* break quits even if exit condition is not correct, it exits the loop

  ``` python
  # m and n, you have to find the first multiple of 7 between m and n
  m = 1000
  n = 1100
  i = m
  while (i<n):
    if i%7 == 0:
      print(i) # print first multiple
      break # rem break to print all multiples
    i+=1
  ```



## continue 

* whenever it is there in loop, rest of code below is skipped and it goes back to the first line 

* skips conditon when continue keyword is encountered

  ```python
  i = 1
  while i <= 20:
    if i%3==0: # this is true
      continue
    print(i)
    i+=1
  ```

* you can use debug feature in python to execute step by step, one at a time
* continue moves up, step back to beginning of the loop 



## if/else example

* tell me how much water is there in the bucket we filled?

  * check if loop completed normally or was break executed in between

* eloborate the bucket example:

  * bucket is 30l, if we are filling with tap, **stop condition i**s when bucket is full
  * **break condition** is when tap stops

* ```python
  i = 1
  while i < 6:
    print(i)
    if i%3==0:
      break
    i+=1
  else: # here we're using while else, not if
    print("i is greater than 6")
  ```



## functions (*important)

* function is a block of code which only runs whenever it is called

* ```python
  a = 13
  print(type(a))
  # takes in var as input, prints the name of data type of value
  ```

* real life example -- like vending machine which spits out food, when we feed it money 



### pros of using function:

* managable 
* avoids repetition (kiss principle)
* modularity



### types of functions:

1. some *built-in* functions examples -- type(), print(), str(), int(), input(), chr(), ord(), range()

   * these functions are baked inside python, they are used a lot, present in python by default

2. *module* functions -- mathematics, perm&comb, time&date

   ```python
   # square root from math module
   from math import sqrt
   print(sqrt(16))
   
   # date and time from datetime module
   date1 = datetime.now()
   print(date1)
   ```

3. *user-defined* functions -- custom functions, user created functions for custom scenarios for our requirements

   ```python
   # temp conversion
   def cel_to_far(far_temp):
     # return((5/9)*(far_temp-32))
     print((5/9)*(far_temp-32))
   # call the function
   cel_to_far(212)
   ```

   * function returns *none* when nothing is returned from a function



## argument, parameter of a function

* let's define a power function

  ```python
  def power_func(a, b): # parameters
    return a ** b
  power_val = power_fn(2, 3) # arguments
  print(power_val)
  ```

* parameter is stating in function def what var we need for this particular function to execute

* argument is value that we give to the function, which are placed into parameters



## default arguments

* if no value of argument is defined, it is only logical that we return only same value 

  ``` python
  def power_func(a, b=1): # parameter b has default value of 1 here
    return a ** b
  power_val = power_fn(2) # arguments
  print(power_val)
  ```

* if we provide argument val it will overwrite the default value

  ``` python
  def message(name = "rahul"):
    print("happy " + name + "!")
  message() ## will use default arugment rahul
  ```

  

  ---

  end of lecture 9