#include <stdio.h>
#include <string.h>

int main() {
    char s[1000];
    scanf("%s", s);

    int freq[26] = {0};

    // Step 1: count frequency
    for (int i = 0; i < strlen(s); i++) {
        freq[s[i] - 'a']++;
    }

    // Step 2: find first non-repeating
    for (int i = 0; i < strlen(s); i++) {
        if (freq[s[i] - 'a'] == 1) {
            printf("%c", s[i]);
            return 0;
        }
    }

    // Step 3: if none found
    printf("$");
    return 0;
}
