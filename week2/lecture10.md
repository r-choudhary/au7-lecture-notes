# week 02 / day 05

# lecture 10

## function

* example 1
    ```python
    def power_fn(a, b=1):
        return a**b
    
    a = power_fn(3, 2)
    ```
* example 2
    ```python
    def happyBirthday(name):
        print("happy birthday ", name)
    a = happyBirthday("rahul")
    print(a)
    print(type(a)
    ```
* if something is written below return statement in function, it is ignored during execution
* return is used instead of print, since we use functions to pass data from one code block to another
* pass -- keyword used to ignore code inside a loop, condition, etc

## list
* define -- list is an *ordered sequence* of *same or different data type* items that are enclosed in *square brackets*
* example -- grocery shopping, with list in order you want to purchase them
    ```
    a_list = [1, 2, 3, 4]
    print(a_list)
    ```
* list is printed in ordered fashion, as it is stored

### indexing in lists
* list supports indexing
* what's indexing?
    ```python
    list[2] 
    
    # output
    $ 3
    ```
* right side indexing/negative indexing
    ```python
    list[-1] 
    
    # output
    $ 4
    ```

## slicing
* example
    ```python
    List = [1, 2, 3, 4]
    print(list[1:3))
    
    # output
    $ [2, 3]
    ```
* list is mutable, that is, list values can be changed even to data types which are different than original data
    ```python
    a_list = ["h", "i"]
    a_list[2] = True 
    
    # runs with error
    ```
## adding elements to list
1. append()
    ```python
    list = [1, 2, 3]
    list.append(True)
    print(list)
    
    # output
    $ [1, 2, 3, True]
    ```
    * can only work to add one element at a time   

2. insert(index, item)
    * choose position to insert element into 
    ```python
    list = [1, 2, 3, 4]
    list.insert(2, True)
    print (list)
    
    # output
    # [1, 2, True, 3, 4]
    
    # negative index
    list.insert(-3, True)
    print (list)
    
    # output
    # [1, True, 3, 4]
    ```
3. extend()
    * add multiple elements to a list a same time
    ```python
    list = [1,2,3,4,5]
    list.extend([True, 'Rahul', 8, 9])
    
    # output
    # [1, 2, 3, 4, 5, True, Rahul, 8, 9)
    ```
    * adding multiple elements to particular list at same time to a particular index is not possible
    * speed of access -- append >> insert >> extend 

## removing elements from list
1. pop()
    ```python
    list = [1,2,3]
    a = list.pop(4) 
    print(a)
    print(List)
    ```
    *  default argument for pop is index = -1, so removes last element from list when no argument is provided
2. del 
    * used to remove a subset of list, can be more than 1 element unlike pop()
    ```python
    list = [1,2,3,4, 5]
    
    del list[2:4]
    print(list)
    ```
    * delete the entire list?
    ```
    del list[::1] # deletes entire list
    ```
    
3. remove()
   * takes in the value and removes its first occurence from the list 
    ```python
    list = [1,2,3]
    list.remove(2)
    
    # output
    # [1, 3]
    ```
    * used for removing duplicates
    
## sorting (*IMPORTANT)
*refer -- https://visualgo.net/bn/sorting*

1. selection sort
    ```python
    list = [1, 2, 3]
    n = len(list)
    for i in range(n-1):
        min = list[i]
        for j in range(i+1, n):
        if list[j]<min:
            min = list[j]
            minIndex = j
        list[i], list[minIndex] = list [minIndex], list[i]
    ```

## tuple
* define -- ordered sequence of same for different items enclosed in ()
    ```python
    tuple = (1,2,3,4)
    print(type(tuple))
    print(tuple)
    
    # output
    (1, 2, 3, 4)
    ```
    
    * note -- tuple is not mutable, values stored cannot be changed
    * supports same operations as lists
    
* why do we have a tuple?
    * faster to process
    * used in indexes of databases, geolocation
 
 ## multi level indexing
* to access sub level of a tuple
    ```python
    print(t[1])
    print(t[1:3])
    LL = [1,2,3,4, [True, False, ["str", "ing"]]]
    
    # access sub level
    print(LL[-1][-1][1][0])
    ```

## tuple functions
*same functions works for both list and tuple*
1. len()
2. max(t) -- prints maximum value in tuple
3. min(t) -- print minimum value in tuple
4. cmp(tup1, tup2) -- outputs boolean true or false, after comparing tuple 1, tuple 2
<br>
---
*end of lecture 10*