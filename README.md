# Домашнее задание к работе 9
## Условие задачи
<b>Варинат 8</b>

Написать программу, выводящую на экран заданную
геометрическую фигуру, нарисованную с помощью заданного с клавиатуры
символа.

<img width="799" height="280" alt="image" src="https://github.com/user-attachments/assets/f3dcd04d-afbf-47c8-a040-29b48ce67e6e" />

## 1. Реализация программы
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
## 2. Результаты работы программы
```
Введите угол SOT (a) в градусах: 20
Введите длину стороны OT (s): 34
Введите символ заполнения: .

Треугольник OST:
Угол SOT=20гр., Сторона OT=34

                         ...
                      ......
                   ..........
                 .............
              .................
           ....................
         .......................
      ...........................
    ..............................
..................................

D:\Алгоритмизация и программирование\Laba9_DZ\x64\Debug\Laba9_DZ.exe (процесс 4504) завершил работу с кодом 0.
Нажмите любую клавишу, чтобы закрыть это окно…

```
<img width="472" height="440" alt="image" src="https://github.com/user-attachments/assets/7b025e66-4251-4bcd-8adb-8d813d2a58ec" />


## 3. Информация о разработчике
> З.Д. бИЦ-251
