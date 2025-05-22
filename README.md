# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1. Start the program.
2. Read two numbers.
3. Calculate the area of rectangle using the formula area=(x)(*y)
4. Display the result.
5. Stop the program.

## PROGRAM
```
#include <stdio.h>
int main() {
    float length, width, area;
    float *ptrLength, *ptrWidth;
    ptrLength = &length;
    ptrWidth = &width;
    scanf("%f", ptrLength);
    scanf("%f", ptrWidth);
    area = (*ptrLength) * (*ptrWidth);
    printf("Area of rectangle = %f sq. units\n", area);
    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/b387fdcc-e19e-459b-b80a-c01cedd13f92)

## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C program to get and print array of characters using malloc() and free()

## ALGORITHM
1. Start.
2. Declare an integer `n` and a character pointer `charArray`.
3. Read the size `n` (number of characters to input).
4. Allocate memory for `n` characters using `malloc`.
5. If memory allocation fails, display an error message and exit.
6. Use a loop to input `n` characters from the user.
7. Use another loop to print the `n` characters.
8. Print a newline.
9. Free the allocated memory.
10. End.


## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, i;
    char *charArray;
    scanf("%d", &n);
    charArray = (char *)malloc(n * sizeof(char));
    if (charArray == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }
    for (i = 0; i < n; i++) {
        scanf(" %c", &charArray[i]);
    }
    for (i = 0; i < n; i++) {
        printf("%c", charArray[i]);
    }
    printf("\n");
    free(charArray);

    return 0;
}
```
## OUTPUT

![image](https://github.com/user-attachments/assets/a631af0b-7728-4f51-9883-ca560967abd0)

## RESULT
Thus the program to get and print array of characters using malloc() and free()

# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM


## OUTPUT


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM


 ## OUTPUT

 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM


## OUTPUT

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


