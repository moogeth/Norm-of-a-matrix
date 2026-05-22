# Norm of a matrix
## Aim
To write a program to find the 1-norm, 2-norm and infinity norm of the matrix and display the result in two decimal places.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
	1. Get the input matrix using np.array()   
    2. Find the 2-norm of the matrix using np.linalg.norm()
	3. Print the norm of the matrix in two decimal places.
## Program:
```Python
# Register No:
# Developed By:
# 1-Norm of a Matrix

'''
devoloped by : Moogethsivan G G 

reg no: 212225040259
'''



A = eval(input())

rows = len(A)
cols = len(A[0])

max_sum = 0

for j in range(cols):
    col_sum = 0
    for i in range(rows):
        col_sum += abs(A[i][j])

    if col_sum > max_sum:
        max_sum = col_sum

print(f"{max_sum:.2f}")


# 2-Norm of a Matrix
'''
Program to find 2-norm of a matrix.
Developed by: Moogethshivan G G 
RegisterNumber: 212225040259
'''
import math

A = eval(input())


AT = list(zip(*A))


B = []
for i in range(len(AT)):
    row = []
    for j in range(len(A[0])):
        s = 0
        for k in range(len(A)):
            s += AT[i][k] * A[k][j]
        row.append(s)
    B.append(row)


a = B[0][0]
b = B[0][1]
c = B[1][0]
d = B[1][1]

trace = a + d
det = a * d - b * c

lambda_max = (trace + math.sqrt(trace**2 - 4 * det)) / 2

l2_norm = math.sqrt(lambda_max)

print(f"{l2_norm:.2f}")



# Infinity Norm of a Matrix

'''
Program to find 2-norm of a matrix.
Developed by: Moogethshivan G G 
RegisterNumber: 212225040259
'''


A = eval(input())

max_sum = 0

for row in A:
    row_sum = 0
    for val in row:
        row_sum += abs(val)

    if row_sum > max_sum:
        max_sum = row_sum

print(f"{max_sum:.2f}")



```
## Output:
### 1-Norm of a Matrix
<img width="1920" height="1080" alt="Screenshot (45)" src="https://github.com/user-attachments/assets/181cbe81-01d1-41f2-8147-e4401c60a705" />


### 2-Norm of a Matrix
<img width="1920" height="1080" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/b9e6c34a-7506-442e-94e5-04bbb62b0912" />


### Infinity Norm of a Matrix
<img width="1920" height="1080" alt="Screenshot (47)" src="https://github.com/user-attachments/assets/15498624-875e-43b0-80db-edc5f301db18" />


## Result
Thus the program for 1-norm, 2-norm and Infinity norm of a matrix are written and verified.
