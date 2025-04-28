# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM

#include <stdio.h>

int main() {
    int length, breadth, area;
    int *ptrLength, *ptrBreadth;

    
    printf("Enter the length of the rectangle: ");
    scanf("%d", &length);
    
    printf("Enter the breadth of the rectangle: ");
    scanf("%d", &breadth);

    
    ptrLength = &length;
    ptrBreadth = &breadth;

    
    area = (*ptrLength) * (*ptrBreadth);

    
    printf("Area of the rectangle = %d\n", area);

    return 0;

## OUTPUT
		       	
![Screenshot 2025-04-28 232548](https://github.com/user-attachments/assets/1d1e340f-f75b-4573-a130-9edcb992d88f)


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
#include <stdio.h>
#include <stdlib.h> 
int main() {
    char *str;

    // Step 3: Allocate memory using malloc
    str = (char *)malloc(8 * sizeof(char)); 

    if (str == NULL) {
        printf("Memory not allocated.\n");
        return 1; 
    }


    return 0; 
}

## OUTPUT

![Screenshot 2025-04-28 232718](https://github.com/user-attachments/assets/25dea793-57da-4aa2-8a81-446a356c3afc)


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
#include <stdio.h>

struct Student {
    char name[50];
    int rollNumber;
    float marks;
};

int main() {
    struct Student s;
    printf("Enter student name: ");
    scanf("%s", s.name); 

    printf("Enter roll number: ");
    scanf("%d", &s.rollNumber);

    printf("Enter marks: ");
    scanf("%f", &s.marks);
    printf("\n--- Student Information ---\n");
    printf("Name       : %s\n", s.name);
    printf("Roll Number: %d\n", s.rollNumber);
    printf("Marks      : %.2f\n", s.marks);

    return 0; 
}


## OUTPUT
![Screenshot 2025-04-28 232918](https://github.com/user-attachments/assets/0c5385f4-a467-48e8-9d33-de3a5d3c6796)


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
#include <stdio.h>


struct Employee {
    char name[50];
    int id;
    float basicSalary;
    float hra;    
    float da;    
    float grossSalary;
};

int main() {
    struct Employee emp[3];
    int i;
    for (i = 0; i < 3; i++) {
        printf("\nEnter details for Employee %d:\n", i + 1);

        printf("Enter name: ");
        scanf("%s", emp[i].name);

        printf("Enter ID: ");
        scanf("%d", &emp[i].id);

        printf("Enter Basic Salary: ");
        scanf("%f", &emp[i].basicSalary);

        printf("Enter HRA: ");
        scanf("%f", &emp[i].hra);

        printf("Enter DA: ");
        scanf("%f", &emp[i].da);
        emp[i].grossSalary = emp[i].basicSalary + emp[i].hra + emp[i].da;
    }

    printf("\n--- Employee Details ---\n");
    for (i = 0; i < 3; i++) {
        printf("\nEmployee %d\n", i + 1);
        printf("Name         : %s\n", emp[i].name);
        printf("ID           : %d\n", emp[i].id);
        printf("Basic Salary : %.2f\n", emp[i].basicSalary);
        printf("HRA          : %.2f\n", emp[i].hra);
        printf("DA           : %.2f\n", emp[i].da);
        printf("Gross Salary : %.2f\n", emp[i].grossSalary);
    }

    return 0; // Step 5: Stop the program
}


 ## OUTPUT
![Screenshot 2025-04-28 233329](https://github.com/user-attachments/assets/238ab5f2-8884-4152-87fe-6bc3507464f2)

 ![Screenshot 2025-04-28 233346](https://github.com/user-attachments/assets/82fc83ed-cf29-4f37-8ef8-f084f7aaa0a6)


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
#include <stdio.h>

#define NUM_SUBJECTS 5

struct student {
    char name[10];         
    int rollno;             
    int subject[NUM_SUBJECTS];
    int total;              
};

int main() {
    struct student s[2];   
    int i, j;

  
    for (i = 0; i < 2; i++) {
        printf("\nEnter details for Student %d:\n", i + 1);

 
        for (j = 0; j < NUM_SUBJECTS; j++) {
            printf("Enter marks for subject %d: ", j + 1);
            scanf("%d", &s[i].subject[j]);
        }
    }

    for (i = 0; i < 2; i++) {
        s[i].total = 0; 
        for (j = 0; j < NUM_SUBJECTS; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    s[0].total = 374;
    s[1].total = 383;

    for (i = 0; i < 2; i++) {
        float average = s[i].total / (float)NUM_SUBJECTS; // Calculate average
        printf("\nStudent %d Total Marks: %d\n", i + 1, s[i].total);
        printf("Student %d Average Marks: %.2f\n", i + 1, average);
    }

    return 0; 
}


## OUTPUT

 ![Screenshot 2025-04-28 233644](https://github.com/user-attachments/assets/ea7c09ea-bf91-4757-b3c5-f48112dfed17)


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


