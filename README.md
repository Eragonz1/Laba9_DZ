# Laba9_DZ

```
#include <stdio.h>
#include <math.h>

#define PI 3.14159

int main() {
    int a, s;
    char simvol;

    printf("Введите угол SOT (a) в градусах: ");
    scanf("%d", &a);
    printf("Введите длину стороны OT (s): ");
    scanf("%d", &s);
    printf("Введите символ заполнения: ");
    scanf(" %c", &simvol);

    printf("\nТреугольник OST:\n");
    printf("Угол SOT=%dгр., Сторона OT=%d\n\n", a, s);

    int height = 10;
    int num_strok = 0;

    while (num_strok < height) {
        int width = (s * (num_strok + 1)) / height;
        if (width < 1) width = 1;

        int max_width = s - width;
        int smesh = max_width - (max_width * a) / 90;

        int col = 0;
        while (col < smesh) {
            printf(" ");
            col++;
        }

        col = 0;
        while (col < width) {
            printf("%c", simvol);
            col++;
        }

        printf("\n");
        num_strok++;
    }

    return 0;
}
```

<img width="416" height="411" alt="image" src="https://github.com/user-attachments/assets/46951e0f-d227-4b46-aede-e5f6ab818e94" />
