#include <stdio.h>
#include <pthread.h>
#include <semaphore.h>
#include <unistd.h>
sem_t forks[5];
void *philosopher(void *arg)
{
    int id = *(int *)arg;
    sem_wait(&forks[id]);
    sem_wait(&forks[(id + 1) % 5]);
    printf("Philosopher %d is eating\n", id);
    sleep(1);
    sem_post(&forks[(id + 1) % 5]);
    sem_post(&forks[id]);
    printf("Philosopher %d is thinking\n", id);
    return NULL;
}
int main()
{
    pthread_t t[5];
    int id[5], i;
    for (i = 0; i < 5; i++)
        sem_init(&forks[i], 0, 1);
    for (i = 0; i < 5; i++)
    {
        id[i] = i;
        pthread_create(&t[i], NULL, philosopher, &id[i]);
    }
    for (i = 0; i < 5; i++)
        pthread_join(t[i], NULL);
    for (i = 0; i < 5; i++)
        sem_destroy(&forks[i]);
    return 0;
}
