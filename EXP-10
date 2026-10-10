#include <stdio.h>
#include <sys/ipc.h>
#include <sys/msg.h>
#include <string.h>
struct message {
    long type;
    char text[100];
};
int main() {
    int id;
    struct message m;
    id = msgget(IPC_PRIVATE, IPC_CREAT | 0666);
    m.type = 1;
    strcpy(m.text, "Hello from message queue");
    msgsnd(id, &m, sizeof(m.text), 0);
    msgrcv(id, &m, sizeof(m.text), 1, 0);
    printf("Received: %s\n", m.text);
    msgctl(id, IPC_RMID, NULL);
    return 0;
}
