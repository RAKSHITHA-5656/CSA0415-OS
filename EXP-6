#include <stdio.h>
int main() {
    int n, i, time = 0, done = 0;
    int bt[10], rem[10], pr[10], wt[10], tat[10];
    scanf("%d", &n);
    for (i = 0; i < n; i++) {
        scanf("%d%d", &bt[i], &pr[i]);
        rem[i] = bt[i];
    }
    while (done < n) {
        int k = -1;

        for (i = 0; i < n; i++)
            if (rem[i] > 0 &&
                (k == -1 || pr[i] < pr[k]))
                k = i;
        rem[k]--;
        time++;
        if (rem[k] == 0) {
            done++;
            tat[k] = time;
            wt[k] = tat[k] - bt[k];
        }
    }
    printf("Process\tWT\tTAT\n");
    for (i = 0; i < n; i++)
        printf("P%d\t%d\t%d\n", i+1, wt[i], tat[i]);
    return 0;
}
