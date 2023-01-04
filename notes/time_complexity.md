# Time Complexity of Alogrithm 
  
## Basic Analyzing Alogrithm
  
we should think of alogrithm basically in two parts, first will be the time and the second will be the space
```http
def swap(x,y){
    temp = x; -> 1
    x = y; -> 1
    y = temp; -> 1
}

total time cost will be f(n) = 3

we have 3 variables in this case so that the space will be s(n) = 3

total will be O(n) = 1
```