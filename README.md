# dataScience-Lec2-23-FEB-25
numpy - Continue - Presentation 19

* Array: can't add items to an array, it's defined at the initial and cannot be changed.
* display: need import IPython.display ,pretty print, and add additional info
  ```
   from IPython.display import display
   display(arr)
  ```
* resize(): like reshape- 
  * doesn't return value
  * can fill with size of the origin length is smaller than the new
* min(), max(): return the min and max value from the array
* argmin(),argmax(): return the index of the min and max values in the array
* arr.shape: a parameter and not a function, return the current arr shape as a tuple,
* copy(): make copy of the origin array (deep copy)- the origin array will not be changed.
* access values in array: like in list - `arr[0],arr[-1],arr[:7],arr[0:2],arr[2][4],arr[0][::-1]`
* assign values to elements in array:
  ```
  # the first 10 values change to 100:
  arr[0:10]=100
  ```
* [condition]: access elements with filter: `arr[arr>4]`
  * the condition arr>4 create an arr of true,false if the element answer the condition 
  * return new array
  * works like in python, with operations &(AND),| (OR) :
  * required `()` if you use 2 conditions: `arr[(arr<4)|(arr>7)]`
  * NOT: ~: `arr[~(arr>5)]`= to get all elements except element=5
* operator *: open the inner array to within :
  ```
    arr[*[false]*4]=arr[*[false,false,false,false]=>arr[false,false,false,false] 
  ```
* modulo: get all elements div 2 or div 3 without remain: `arr[(arr%2==0)|(arr%3==0)]`
* save(),load(): save array to a file: np.save('filename.npy, arr) in encryption, nums=np.load('filename'.npy)
* math actions doesn't change the origin array: 
`arr+2` for each element add 2,`arr-2` for each element sub 2.....