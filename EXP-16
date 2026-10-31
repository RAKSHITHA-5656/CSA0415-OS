#include <stdio.h>
struct Employee {
    int id;
    char name[30];
    float salary;
};
int main() {
    FILE *fp;
    struct Employee e;
    int n, pos;
    fp = fopen("employee.dat", "wb+");
    if (fp == NULL) {
        printf("File error");
        return 1;
    }
    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        scanf("%d %29s %f", &e.id, e.name, &e.salary);
        fwrite(&e, sizeof(e), 1, fp);
    }
    scanf("%d", &pos);

    if (pos < 1 || pos > n) {
        printf("Invalid record number");
    } else {
        fseek(fp, (pos - 1) * sizeof(e), SEEK_SET);
        fread(&e, sizeof(e), 1, fp);
         printf("\nEmployee Details\n");
        printf("ID: %d\nName: %s\nSalary: %.2f\n",
               e.id, e.name, e.salary);
    }

    fclose(fp);
    return 0;
}
