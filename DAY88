#include <stdio.h>
#include <stdlib.h>

// function to sort array (simple bubble sort for beginners)
void sort(int arr[], int n) {
    for(int i = 0; i < n-1; i++) {
        for(int j = 0; j < n-i-1; j++) {
            if(arr[j] > arr[j+1]) {
                int temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }
}

// check if we can place k cows with minimum distance = dist
int canPlace(int stalls[], int n, int k, int dist) {
    int count = 1; // first cow
    int lastPos = stalls[0];

    for(int i = 1; i < n; i++) {
        if(stalls[i] - lastPos >= dist) {
            count++;
            lastPos = stalls[i];
        }
        if(count >= k)
            return 1; // possible
    }
    return 0; // not possible
}

int main() {
    int n, k;

    printf("Enter number of stalls and cows:\n");
    scanf("%d %d", &n, &k);

    int stalls[n];

    printf("Enter stall positions:\n");
    for(int i = 0; i < n; i++) {
        scanf("%d", &stalls[i]);
    }

    // sort stalls
    sort(stalls, n);

    int low = 1;
    int high = stalls[n-1] - stalls[0];
    int ans = 0;

    while(low <= high) {
        int mid = (low + high) / 2;

        if(canPlace(stalls, n, k, mid)) {
            ans = mid;        // possible
            low = mid + 1;    // try bigger distance
        } else {
            high = mid - 1;   // reduce distance
        }
    }

    printf("Maximum minimum distance = %d\n", ans);

    return 0;
}
