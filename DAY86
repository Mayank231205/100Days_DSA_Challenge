#include <stdio.h>

int main() {
    long long n;
    scanf("%lld", &n);

    long long left = 0, right = n;
    long long ans = 0;

    while (left <= right) {
        long long mid = left + (right - left) / 2;

        // Avoid overflow
        if (mid <= n / mid) {
            ans = mid;          // valid sqrt
            left = mid + 1;     // try bigger
        } else {
            right = mid - 1;    // go smaller
        }
    }

    printf("%lld\n", ans);

    return 0;
}
