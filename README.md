#include <stdio.h>

#include <stdlib.h>

struct student {

    char name[50];

    int roll_number;

    float marks;

};

int main() {

    struct student s;

    FILE *fptr;

    fptr = fopen("students.txt", "a+");

    if (fptr == NULL) {

        printf("Error opening file.");

        exit(1);

    }

    printf("Enter name: ");

    scanf("%s", s.name);

    printf("Enter roll number: ");

    scanf("%d", &s.roll_number);

    printf("Enter marks: ");

    scanf("%f", &s.marks);

    fprintf(fptr, "%s %d %.2f\n", s.name, s.roll_number, s.marks);

    fclose(fptr);

    return 0;

}
