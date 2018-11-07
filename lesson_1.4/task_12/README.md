# Задача 12

## Условие

Яша плавал в бассейне размером N×M метров и устал. В этот момент он обнаружил, что находится на расстоянии X метров от одного из длинных бортиков (не обязательно от ближайшего) и Y метров от одного из коротких бортиков. Какое минимальное расстояние должен проплыть Яша, чтобы выбраться из бассейна на бортик? 

## Формат входных данных:

Программа получает на вход числа N, M, X, Y. 

## Формат выходных данных

Программа должна вывести число метров, которое нужно проплыть Яше до бортика.

## Sample Input:

23

52

8

43

## Sample Output:

8

``` cpp
#include <iostream>

int main() {
  int n, m, x, y, altX, altY;
    std::cin >> n >> m >> x >> y;
    if (n > m) {
        altX = m - x;
        altY = n - y;
        if ((x > altX) && (y > altY)) {
            if (altX > altY) {
                std::cout << altY;
            } else {
                std::cout << altX;
            }
        } else if ((x > altX) && (y < altY)) {
            if (altX > y) {
                std::cout << y;
            } else {
                std::cout << altX;
            }
        } else if ((x < altX) && (y > altY)) {
            if (x > altY) {
                std::cout << altY;
            } else {
                std::cout << x;
            }
        } else {
            if (x > y) {
                std::cout << y;
            } else {
                std::cout << x;
            }
        }
    } else {
        altX = n - x;
        altY = m - y;
        if ((x > altX) && (y > altY)) {
            if (altX > altY) {
                std::cout << altY;
            } else {
                std::cout << altX;
            }
        } else if ((x > altX) && (y < altY)) {
            if (altX > y) {
                std::cout << y;
            } else {
                std::cout << altX;
            }
        } else if ((x < altX) && (y > altY)) {
            if (x > altY) {
                std::cout << altY;
            } else {
                std::cout << x;
            }
        } else {
            if (x > y) {
                std::cout << y;
            } else {
                std::cout << x;
            }
        }
    }
  return 0;
}
```
