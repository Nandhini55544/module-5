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

# EX-28-BOOKS-INFORMATION-USING-STRUCTURE

## AIM
Write a program to store information of Books (id, name, title and subject) using function with structure.

## ALGORITHM
1. Start
2. Declare a structure variable b of type Book
3. Call function inputBook and pass the address of b
4. Inside inputBook function:
   a. Input book title
   b. Input book name
   c. Input book subject
   d. Input book id
5. Return to main and call displayBook function with b as argument
6. Inside displayBook function:
   a. Print book title
   b. Print book name
   c. Print book subject
   d. Print book id
7. End

## PROGRAM
```
#include <stdio.h>
struct Book {
    char title[50];
    char name[50];
    char subject[50];
    int id;
};
void inputBook(struct Book *b) {
    scanf("%s", b->title);
    scanf("%s", b->name);
    scanf("%s", b->subject);
    scanf("%d", &b->id);
}
void displayBook(struct Book b) {
    printf("Book Title is =%s\n", b.title);
    printf("Book Name is =%s\n", b.name);
    printf("Book Subject is =%s\n", b.subject);
    printf("Book Id is =%d\n", b.id);
}

int main() {
    struct Book b;

    inputBook(&b);
    displayBook(b);

    return 0;
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/feff156f-aad2-4318-b7e7-21cdbb5efa0c)


## RESULT

Thus the program to store books information and display it using structure has been executed successfully
 

# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C program to accept details of 'n' employee(eno, ename, salary) and display the details of employee having highest salary using array of structure.

## ALGORITHM

1. Start
2. Input the number of employees n
3. Declare an array of structure Employee of size n
4. Set max\_salary to 0
5. For i from 0 to n-1 do
   a. Input employee number
   b. Input employee name
   c. Input employee salary
   d. If employee salary > max\_salary, set max\_salary = employee salary
6. Print "Highest salary employee details:"
7. For i from 0 to n-1 do
   a. If employee salary == max\_salary, print employee number, name, and salary
8. End

## PROGRAM
```
#include <stdio.h>
#include <string.h>

struct Employee {
    int eno;
    char ename[50];
    float salary;
};

int main() {
    int n, i;
    scanf("%d", &n);

    struct Employee emp[n];
    float max_salary = 0;
    for(i = 0; i < n; i++) {
        scanf("%d", &emp[i].eno);
        scanf("%s", emp[i].ename);
        scanf("%f", &emp[i].salary);

        if(emp[i].salary > max_salary) {
            max_salary = emp[i].salary;
        }
    }
    printf("Highest salary employee details:");
    for(i = 0; i < n; i++) {
        if(emp[i].salary == max_salary) {
            printf("%d      %s      %.0f", emp[i].eno, emp[i].ename, emp[i].salary);
        }
    }

    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/d6dc6d82-1ddb-45cb-8227-1d236a63ac57)

![image](https://github.com/user-attachments/assets/5f950e76-bf1b-4881-abba-89e1409ad842)

## RESULT
Thus the C program to read and store the data of 3 employees and calculate their highest Salary using the concept of structure has been successfully executed.
 
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
```
#include <stdio.h>

struct student {
    char name[10];
    int rollno;
    int subject[5], total;
};

int main() {
    int n, i, j;
    struct student s[100];

    scanf("%d", &n); 

    for (i = 0; i < n; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
            s[i].total += s[i].subject[j];
        }
    }

    for (i = 0; i < n; i++) {
        printf("%d\n", s[i].total);
    }

    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/716162da-5b6b-4470-8bc9-3c16dfabf7c5)

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


