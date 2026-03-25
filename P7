#include <stdio.h>

int main() {
    char ch, next;

    printf("Enter C code (Ctrl+Z to end):\n");

    while ((ch = getchar()) != EOF) {
        // Check for single-line comment
        if (ch == '/') {
            next = getchar();

            if (next == '/') {
                // Skip till end of line
                while ((ch = getchar()) != '\n' && ch != EOF);
            }
            else if (next == '*') {
                // Skip multi-line comment
                while (1) {
                    ch = getchar();
                    if (ch == '*' && (next = getchar()) == '/')
                        break;
                }
            }
            else {
                putchar(ch);
                putchar(next);
            }
        }
        else {
            putchar(ch);
        }
    }

    return 0;
}
