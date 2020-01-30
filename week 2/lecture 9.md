# week 02 / lecture 9

date -- jan 30, 2020



## cc3 discussed

* ```python
  # solution for lecture 8 cc3
  for i in range(1, 11):
  	print(14*i)
  ```



## while loop

* used for indefinite iternations, when you do not know the exit condition

* regular increment, in each run of loop 

* ```python
  age = 17
  while (age<18):
    print("you are illegal")
    age+=1
  # while is most useful when increments are not regular
  print("thy must drink that beer")
  ```

* exit condition -- to make loop continue to run , we need to iterate e



## break

* real life example of break statement -- if water runs out, bucket may or may not fill depending on time of day when water comes

* break quits even if exit condition is not correct, it exits the loop

* ```python
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

* ```python
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

* eloborate example

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

  