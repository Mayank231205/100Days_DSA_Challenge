#include <stdio.h>

int main() {
    int n, target;

    scanf("%d", &n);

    int arr[100];

    // Input sorted array
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Input target
    scanf("%d", &target);

    int left = 0, right = n - 1;
    int found = -1;

    while (left <= right) {
        int mid = left + (right - left) / 2;

        if (arr[mid] == target) {
            found = mid;
            break;
        }
        else if (arr[mid] < target) {
            left = mid + 1;
        }
        else {
            right = mid - 1;
        }
    }

    printf("%d\n", found);

    return 0;
}
