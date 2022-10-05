# Writeup for Matrix lab1

this was a java .class file

i use this website http://www.javadecompilers.com/ to decompile the file.

```java
import math
import numpy as np
solvethis = "oz]{R]3l]]B#50es6O4tL23Etr3c10_F4TD2"

global lenght
length = int(math.pow(2.0, 3.0) - 2)

def reverse_ecrypt(arrc2, n):
    n2 = 0
    while n2 < length * 2:
        n5 = n2
        n2 += 1
        arrc2[n5] = chr(ord(arrc2[n5]) ^ n)
    arrc = [ None for i in range(length*2) ]
    n3 = (length*2) - 1
    n4 = length*2
 # oz]{R]3l]]B#
    arrc[0] = arrc2[10]
    arrc[1] = arrc2[8]
    arrc[2] = arrc2[6]
    arrc[3] = arrc2[4]
    arrc[4] = arrc2[2]
    arrc[5] = arrc2[0]
    arrc[6] = arrc2[1]
    arrc[7] = arrc2[3]
    arrc[8] = arrc2[5]
    arrc[9] = arrc2[7]
    arrc[10] = arrc2[9]
    arrc[11] = arrc2[11]
    return "".join(arrc)


def reverse_transform(arrc2, n):
    arrc = ["0"]*len("@_1P_@_M57M_nu__51_N017Pyrc3d_x1rt4m")
    i = 0
    while i < n*n:
        arrc[i] = arrc2[int(i / n)][int(i % n)]
        i += 1
    return arrc


def reverse_getArray(arrc, arrc2, n, n2):
    n4 = 0
    n3 = 0
    while n3 < length:
        arrc[n][n3] = arrc2[n4]
        n3 += 1
        n4 += 1
    n3 = 0
    while n3 < length:
        arrc[n2][length - 1 - n3] = arrc2[n4]
        n4 += 1
        n3 += 1
    return arrc

def reverse_solve():
    pone = reverse_ecrypt([*"oz]{R]3l]]B#"], 2)
    ptwo = reverse_ecrypt([*"50es6O4tL23E"], 1)
    pthree = reverse_ecrypt([*"tr3c10_F4TD2"], 0)
    arrc = [ [ None for i in range(length) ] for j in range(length) ]
    arrc = reverse_getArray(arrc,pone, 5, 0)
    arrc = reverse_getArray(arrc,ptwo, 4, 1)
    arrc = reverse_getArray(arrc,pthree, 3, 2)
    i = 0
    j = 0
    arr_t = np.array(arrc).T
    print(arr_t.T)
    arrc = arr_t


    print("".join(reverse_transform(arrc, length)))
reverse_solve()
```


so this does not actually get the flag, but makes an array which needs to be transposed, or you could read it from the debug code.
reading the matrix shows the flag:`SEKAI{m4tr1x_d3cryP710N_15_Fun_M4T3_@2D2D!}`