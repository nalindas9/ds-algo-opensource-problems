There is a new mobile game that starts with consecutively numbered clouds. Some of the clouds are thunderheads and others are cumulus. The player can jump on any cumulus cloud having a number that is equal to the number of the current cloud plus  or . The player must avoid the thunderheads. Determine the minimum number of jumps it will take to jump from the starting postion to the last cloud. It is always possible to win the game.
For each game, you will get an array of clouds numbered  if they are safe or  if they must be avoided.
Example

Index the array from . The number on each cloud is its index in the list so the player must avoid the clouds at indices  and . They could follow these two paths:  or . The first path takes  jumps while the second takes . Return .
Function Description
Complete the jumpingOnClouds function in the editor below.
jumpingOnClouds has the following parameter(s):
int c[n]: an array of binary integers
Returns
int: the minimum number of jumps required
Input Format
The first line contains an integer , the total number of clouds. The second line contains space-separated binary integers describing clouds  where .
Constraints

Output Format
Print the minimum number of jumps needed to win the game.
Sample Input 0
7
0 0 1 0 0 1 0
Sample Output 0
4
Explanation 0:
The player must avoid  and . The game can be won with a minimum of  jumps:
jump(2).png
Sample Input 1
6
0 0 0 0 1 0
Sample Output 1
3
Explanation 1:
The only thundercloud to avoid is . The game can be won in  jumps:
jump(5).png


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

