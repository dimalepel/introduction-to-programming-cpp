# Задача 4

## Условие

Дано натуральное число N. Выведите слово YES, если число N является точной степенью двойки, или слово NO в противном случае.

## Формат входных данных

Вводится натуральное число.

## Формат выходных данных

Выведите ответ на задачу.

## Sample Input 1:

1

## Sample Output 1:

YES

## Sample Input 2:

2

## Sample Output 2:

YES

``` cpp
#include <iostream>

int main() {
  int n, pow = 1, ans = 0;
  std::cin >> n;

  while (pow <= n) {
    if (pow == n) {
      ans = 1;
    }
    pow *= 2;
  }

  if (ans == 1) {
    std::cout << "YES";
  } else {
    std::cout << "NO";
  }

  return 0;
}
```
