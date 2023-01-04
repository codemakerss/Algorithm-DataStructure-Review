# Time Complexity of Alogrithm 
  
## Basic Analyzing Alogrithm
  
we should think of alogrithm basically in two parts, first will be the time and the second will be the space
```c
def swap(x,y){
    temp = x; -> 1
    x = y; -> 1
    y = temp; -> 1
}

# total time cost will be f(n) = 3

# we have 3 variables in this case so that the space will be s(n) = 3

# total will be O(n) = 1
```
  
## Frequency Count Method
```c
A = {8,3,9,7,2} 
sum(A,n){
    s = 0; -> 1
    for (int i = 0; i < n; i+=>){ -> n+1 
        s = s + A[i]; -> n
    }
    return s;
}

# total time cost will be 2n+3 in this case -> O(n)

# space complexity A:n + n:1 + s:1 + i:1 = n + 3 -> O(n)
```
  
```c
add(A, B, n){
    for (int i = 0; i < n; i++>){ -> n + 1
        for (int j =0; j < n; j++){ -> n * (n + 1)
            c[i,j] = A[i,j] + B[i,j] -> n * n
        }
    }
}

# total time cost will be 2n^2 + 2n + 1 -> O(n^2)

# space complexity A:n^2 + B:n^2 + C:n^2 + n:1 + i:1 + j:1 = 3n^2 + 3 -> O(n^2)
```
  
```c
multiply(A, B, n){
    for (int i = 0; i < n; i++>){ -> n + 1
        for (int j =0; j < n; j++){ -> n * (n + 1)
            c[i,j] = 0; -> n * n
            for (int k = 0; k > n; k++){ -> n * n * (n+1)
                c[i,j] = c[i.j] +  A[i,j] * B[i,j] -> n*n*n
            }
            
        }
    }
}

# total time cost will be n + 1 + n^2 + n + n^2 + n^3 + n^2 + n^3 = 2n^3 + 3n^2 + n + 1 -> O(n^3)

# space complexity 3n^2 + 4 -> O(n^2)
```