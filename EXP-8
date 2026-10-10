
#include <stdio.h>

int main() {
    int n, i, tq, time = 0, done;
    int bt[10], rem[10], wt[10], tat[10];

    printf("Enter number of processes: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        printf("Burst time of P%d: ", i+1);
        scanf("%d", &bt[i]);
        rem[i] = bt[i];
    }

    printf("Enter time quantum: ");
    scanf("%d", &tq);

    do {
        done = 1;

        for (i = 0; i < n; i++) {
            if (rem[i] > 0) {
                done = 0;

                if (rem[i] > tq) {
                    time += tq;
                    rem[i] -= tq;
                } else {
                    time += rem[i];
                    rem[i] = 0;
                    tat[i] = time;
                    wt[i] = tat[i] - bt[i];
                }
            }
        }
    } while (!done);

    printf("Process\tWT\tTAT\n");
    for (i = 0; i < n; i++)
        printf("P%d\t%d\t%d\n", i+1, wt[i], tat[i]);

    return 0;
}
