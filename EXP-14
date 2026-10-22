#include <stdio.h>
#include <string.h>
int main() {
    char files[20][30], name[30];
    int n=0, ch, i, found;
    while(1) {
        printf("\n1.Create 2.Search 3.Display 4.Exit\n");
        scanf("%d",&ch);
        if(ch==1) {
            printf("Enter file name: ");
            scanf("%29s",name);
            found=0;
            for(i=0;i<n;i++)
                if(strcmp(files[i],name)==0) found=1;
            if(found) printf("File already exists\n");
            else if(n<20) {
                strcpy(files[n++],name);
                printf("File created\n");
            } else printf("Directory full\n");
        }
        else if(ch==2) {
            printf("Enter file name: ");
            scanf("%29s",name);
            found=0;
            for(i=0;i<n;i++)
                if(strcmp(files[i],name)==0) found=1;
            if(found) printf("File found\n");
            else printf("File not found\n");
        }
        else if(ch==3) {
            printf("Files:\n");
            for(i=0;i<n;i++) printf("%s\n",files[i]);
        }
        else if(ch==4) break;
        else printf("Invalid choice\n");
    }
    return 0;
}
