#include <stdio.h>
#include <string.h>
int main() {
    char users[10][20], files[10][10][20];
    char user[20], file[20];
    int count[10]={0}, nu=0, ch, i, j, u, found;
    while(1) {
        printf("\n1.Add User 2.Create File 3.Search File");
        printf("\n4.Display Files 5.Exit\n");
        scanf("%d",&ch);
        if(ch==1) {
            if(nu==10) {
                printf("User limit reached\n");
                continue;
            }
            scanf("%19s",user);
            found=0;
            for(i=0;i<nu;i++)
                if(strcmp(users[i],user)==0) found=1;
            if(found) printf("User already exists\n");
            else {
                strcpy(users[nu++],user);
                printf("User directory created\n");
            }
        }
        else if(ch>=2 && ch<=4) {
            scanf("%19s",user);
            u=-1;
            for(i=0;i<nu;i++)
                if(strcmp(users[i],user)==0) u=i;
            if(u==-1) {
                printf("User not found\n");
                continue;
            }
            if(ch==2) {
                if(count[u]==10) {
                    printf("Directory full\n");
                    continue;
                }
                scanf("%19s",file);
                found=0;
                for(j=0;j<count[u];j++)
                    if(strcmp(files[u][j],file)==0) found=1;
                if(found) printf("File already exists\n");
                else {
                    strcpy(files[u][count[u]++],file);
                    printf("File created\n");
                }
            }
            else if(ch==3) {
                scanf("%19s",file);
                found=0;
                for(j=0;j<count[u];j++)
                    if(strcmp(files[u][j],file)==0) found=1;
                if(found) printf("File found\n");
                else printf("File not found\n");
            }
            else {
                printf("Files of %s:\n",users[u]);
                for(j=0;j<count[u];j++)
                    printf("%s\n",files[u][j]);
            }
        }
        else if(ch==5) break;
        else printf("Invalid choice\n");
    }
    return 0;
}
