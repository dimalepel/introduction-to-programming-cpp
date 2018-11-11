# Задача 13

## Условие

Дано три числа. Упорядочите их в порядке неубывания. 

## Формат входных данных:

Вводятся три числа. 

## Формат выходных данных

Выведите ответ на задачу. 

## Sample Input:

1

2

1

## Sample Output:

1 1 2

``` cpp
#include <iostream>

int main() {
  int a, b, c, k, l, m; 
    std::cin >> a >> b >> c;
    if (a > b) {
        if (a > c) {
            m = a;
            if (b > c) {
                l = b;
                k = c;
            } else if (b < c) {
                k = b;
                l = c;
            } else {
                k = b;
                l = b;
            }
        } else if (a < c) {
            m = c;
            l = a;
            k = b;
        } else {
            m = a;
            l = a;
            k = b;
        }
    } else if (a < b) {
        if (b > c) {
            m = b;
            if (a > c) {
                l = a;
                k = c;
            } else if (a < c) {
                l = c;
                k = a;
            } else {
                k = a;
                l = a;
            }
        } else if (b < c) {
            m = c;
            l = b;
            k = a;
        } else {
            m = c;
            l = c;
            k = a;
        }
    } else {
        if (a > c) {
            k = c;
            l = a;
            m = a;
        } else if (a < c) {
            k = a;
            l = a;
            m = c;
        } else {
            k = a;
            l = a;
            m = a;
        }
    }
    std::cout << k << " " << l << " " << m;
  return 0;
}
```
