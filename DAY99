#include <stdio.h>
#include <stdlib.h>

// structure to store position and time
typedef struct {
    int position;
    double time;
} Car;

// comparator for sorting in descending order of position
int compare(const void* a, const void* b) {
    Car* c1 = (Car*)a;
    Car* c2 = (Car*)b;
    return c2->position - c1->position;
}

int main() {
    int n, target;

    printf("Enter number of cars:\n");
    scanf("%d", &n);

    int position[n], speed[n];

    printf("Enter target distance:\n");
    scanf("%d", &target);

    printf("Enter positions:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &position[i]);
    }

    printf("Enter speeds:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &speed[i]);
    }

    Car cars[n];

    // compute time
    for (int i = 0; i < n; i++) {
        cars[i].position = position[i];
        cars[i].time = (double)(target - position[i]) / speed[i];
    }

    // sort by position descending
    qsort(cars, n, sizeof(Car), compare);

    int fleets = 0;
    double maxTime = 0;

    for (int i = 0; i < n; i++) {
        if (cars[i].time > maxTime) {
            fleets++;
            maxTime = cars[i].time;
        }
    }

    printf("Number of car fleets = %d\n", fleets);

    return 0;
}
