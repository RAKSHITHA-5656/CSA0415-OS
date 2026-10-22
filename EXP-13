#include <stdio.h>
int main() {
    int b[10], p[10], alloc[10], m, n, choice, i, j, best;
    scanf("%d", &m);
    for(i=0;i<m;i++) {
        scanf("%d", &b[i]);
    scanf("%d", &n);
    for(i=0;i<n;i++) {
        printf("Process %d size: ", i+1);
        scanf("%d", &p[i]);
        alloc[i] = -1;
    }
    printf("1.First Fit  2.Best Fit  3.Worst Fit: ");
    scanf("%d", &choice);
    for(i=0;i<n;i++) {
        best = -1;
        for(j=0;j<m;j++) {
            if(b[j] >= p[i]) {
                if(choice == 1) { best=j; break; }
                if(best == -1 ||
                  (choice == 2 && b[j] < b[best]) ||
                  (choice == 3 && b[j] > b[best]))
                    best=j;
            }
        }
        if(best != -1) {
            alloc[i]=best;
            b[best]-=p[i];
        }
    }
    printf("\nProcess\tSize\tBlock\n");
    for(i=0;i<n;i++) {
        printf("%d\t%d\t",i+1,p[i]);
        if(alloc[i]==-1) printf("Not allocated\n");
        else printf("%d\n",alloc[i]+1);
    }
    return 0;
}
