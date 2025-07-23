There is a large pile of socks that must be paired by color. Given an array of integers representing the color of each sock, determine how many pairs of socks with matching colors there are.
Example


There is one pair of color  and one of color . There are three odd socks left, one of each color. The number of pairs is .
Function Description
Complete the sockMerchant function in the editor below.
sockMerchant has the following parameter(s):
int n: the number of socks in the pile
int ar[n]: the colors of each sock
Returns
int: the number of pairs
Input Format
The first line contains an integer , the number of socks represented in .
The second line contains  space-separated integers, , the colors of the socks in the pile.
Constraints

 where 
Sample Input
STDIN                       Function
-----                       --------
9                           n = 9
10 20 20 10 10 30 50 10 20  ar = [10, 20, 20, 10, 10, 30, 50, 10, 20]
Sample Output
3
Explanation
sock.png
<img width="1220" height="682" alt="image" src="https://github.com/user-attachments/assets/08d42291-2873-4a5c-93e3-01da64b11b21" />

There are three pairs of socks.


# Code
```
#!/bin/python3

import math
import os
import random
import re
import sys

def sockMerchant(n, ar):
    # Write your code here
    freq_dict = dict()
    pairs = 0
    for i in range(len(ar)):
        if ar[i] not in freq_dict.keys():
            freq_dict[ar[i]] = 1
        else:
            freq_dict[ar[i]] = freq_dict[ar[i]] + 1
    print('freq dict: {}'.format(freq_dict))
    for i in freq_dict.values():
        pairs += i//2
    return pairs

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    n = int(input().strip())

    ar = list(map(int, input().rstrip().split()))

    result = sockMerchant(n, ar)

    fptr.write(str(result) + '\n')

    fptr.close()
```

