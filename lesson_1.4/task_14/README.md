# Задача 14

## Условие

Есть две коробки, первая размером A1×B1×C1, вторая размером A2×B2×C2. Определите, можно ли разместить одну из этих коробок внутри другой, при условии, что поворачивать коробки можно только на 90 градусов вокруг ребер.

## Формат входных данных:

Программа получает на вход числа A1, B1, C1, A2, B2, C2. 

## Формат выходных данных

Программа должна вывести одну из следующих строчек:
Boxes are equal, если коробки одинаковые,
The first box is smaller than the second one, если первая коробка может быть положена во вторую,
The first box is larger than the second one, если вторая коробка может быть положена в первую,
Boxes are incomparable, во всех остальных случаях.

## Sample Input 1:

1

2

3

3

2

1

## Sample Output 1:

Boxes are equal

## Sample Input 2:

2

2

3

3

2

1

## Sample Output 2:

The first box is larger than the second one

``` cpp
#include <iostream>

int main() {
  int a_1, b_1, c_1; // box 1
	int a_2, b_2, c_2; // box 2
	std::cin >> a_1 >> b_1 >> c_1 >> a_2 >> b_2 >> c_2;
	if ((a_1 == a_2 and b_1 == b_2 and c_1 == c_2) or
			(a_1 == a_2 and b_1 == c_2 and c_1 == b_2) or
			(a_1 == c_2 and b_1 == a_2 and c_1 == b_2) or
			(a_1 == b_2 and b_1 == a_2 and c_1 == c_2) or
			(a_1 == b_2 and b_1 == c_2 and c_1 == a_2) or
			(a_1 == c_2 and b_1 == b_2 and c_1 == a_2)) {
					std::cout << "Boxes are equal";
			}
	else if ((a_1 <= a_2 and b_1 <= b_2 and c_1 <= c_2) or
			(a_1 <= a_2 and b_1 <= c_2 and c_1 <= b_2) or
			(a_1 <= c_2 and b_1 <= a_2 and c_1 <= b_2) or
			(a_1 <= b_2 and b_1 <= a_2 and c_1 <= c_2) or
			(a_1 <= b_2 and b_1 <= c_2 and c_1 <= a_2) or
			(a_1 <= c_2 and b_1 <= b_2 and c_1 <= a_2)) {
					std::cout << "The first box is smaller than the second one";
			}
	else if ((a_1 >= a_2 and b_1 >= b_2 and c_1 >= c_2) or
			(a_1 >= a_2 and b_1 >= c_2 and c_1 >= b_2) or
			(a_1 >= c_2 and b_1 >= a_2 and c_1 >= b_2) or
			(a_1 >= b_2 and b_1 >= a_2 and c_1 >= c_2) or
			(a_1 >= b_2 and b_1 >= c_2 and c_1 >= a_2) or
			(a_1 >= c_2 and b_1 >= b_2 and c_1 >= a_2)) {
					std::cout << "The first box is larger than the second one";
			}
	else {
			std::cout << "Boxes are incomparable";
	}
  return 0;
}
```
