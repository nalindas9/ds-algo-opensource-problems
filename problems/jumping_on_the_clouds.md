<img width="1470" height="915" alt="image" src="https://github.com/user-attachments/assets/1138e6a4-0c9d-41bb-92ed-1b522f614f67" />

```
#!/bin/python3

import math
import os
import random
import re
import sys


def jumpingOnClouds(c):
    # Write your code here
    # shortest_path_length_single_jump = 0
    # for i in range(len(c)):
    #     if c[i] == 1:
    #         continue
    #     shortest_path_length_single_jump = shortest_path_length_single_jump + 1
    # print("shortest_path_length_single_jump: {}".format(shortest_path_length_single_jump))
    # shortest_path_length_double_jump = 0
    # for i in range(0, len(c), 2):
    #     if c[i] == 1:
    #         continue
    #     shortest_path_length_double_jump = shortest_path_length_double_jump + 1
    # print("shortest_path_length_double_jump: {}".format(shortest_path_length_double_jump))
    shortest_path_len = 0
    i = 0
    while i < n-1:
        if i + 2 >= n or c[i+2] == 1:
            i = i+1
            shortest_path_len += 1
        else:
            i = i + 2
            shortest_path_len += 1
    return shortest_path_len
        

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    n = int(input().strip())

    c = list(map(int, input().rstrip().split()))

    result = jumpingOnClouds(c)

    fptr.write(str(result) + '\n')

    fptr.close()
```

