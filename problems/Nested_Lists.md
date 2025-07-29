Given the names and grades for each student in a class of  students, store them in a nested list and print the name(s) of any student(s) having the second lowest grade.
Note: If there are multiple students with the second lowest grade, order their names alphabetically and print each name on a new line.
Example

The ordered list of scores is , so the second lowest score is . There are two students with that score: . Ordered alphabetically, the names are printed as:
alpha
beta
Input Format
The first line contains an integer, , the number of students.
The  subsequent lines describe each student over  lines.
- The first line contains a student's name.
- The second line contains their grade.
Constraints

There will always be one or more students having the second lowest grade.
Output Format
Print the name(s) of any student(s) having the second lowest grade in. If there are multiple students, order their names alphabetically and print each one on a new line.
Sample Input 0
5
Harry
37.21
Berry
37.21
Tina
37.2
Akriti
41
Harsh
39
Sample Output 0
Berry
Harry
Explanation 0
There are  students in this class whose names and grades are assembled to build the following list:
python students = [['Harry', 37.21], ['Berry', 37.21], ['Tina', 37.2], ['Akriti', 41], ['Harsh', 39]]
The lowest grade of  belongs to Tina. The second lowest grade of  belongs to both Harry and Berry, so we order their names alphabetically and print each name on a new line.

```
if __name__ == '__main__':
    python_students = list()
    for _ in range(int(input())):
        name = input()
        score = float(input())
        python_students.append([name, score])
    python_students = sorted(python_students, key=lambda x: x[1])
    lowest_score = python_students[0][1]
    second_lowest_score = None
    
    names_with_lowest_scores = list()
    for i in range(len(python_students)):
        if python_students[i][1] == lowest_score:
            second_lowest_score = python_students[i+1][1]
            continue
        else:
            if python_students[i][1] == second_lowest_score:
                names_with_lowest_scores.append(python_students[i][0])
    names_with_lowest_scores = sorted(names_with_lowest_scores)
    for name in names_with_lowest_scores:
        print(name)

```
