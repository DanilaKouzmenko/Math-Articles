# Периодические дроби
В этой статье я разберу базовые операции с периодическими дробями.
## Основы
Периодическая дробь - это такое число, где часть после запятой бесконечно повторяется. Записывается как десятичная дробь с периодической частью в скобках. То есть $0.(1)=0.111111111111...$

Также можно выразить обычные числа как периодические.
$1=1.00000...=1.(0)$, $-0.51=-0.510000\dots=-0.51(0)$ и расширить периодическую часть $1.(2)=1.22222222\dots=1.(22)=1.(222)$

Можно периодическое число перевести в формат обычной дроби таким образом:
$1.(1234)=x\iff 1.(1234) \cdot 10000=11234.(1234)=10000x\iff 11234.\cancel{(1234)}-1.\cancel{(1234)}=10000x-x\iff 11233=9999x\iff x=\frac{11233}{9999}$
Для записи периодических чисел я буду писать букву, обозначающую 1 цифру в таком виде: $a=3;b=4; \overline{ab}=34$
### Быстрый перевод
$\overline{a.(b)}=x\iff\overline{ab.(b)}=10x\iff\overline{ab.\cancel{(b)}}-\overline{a.\cancel{(b)}}=10x-x=9x\iff x=\frac{10a+b-a}{9}=\frac{9a+b}{9}=a+\frac{b}{9}$
Другой случай
$\overline{a.(bc)}=x\iff\overline{abc.(bc)}=100x\iff\overline{abc.\cancel{(bc)}}-\overline{a.\cancel{(bc)}}=100x-x=99x\iff x=\frac{\overline{abc}-a}{99}=\frac{100a+10b+c-a}{99}=\frac{99a+10b+c}{99}=a+\frac{10b+c}{9}$
Чтобы быстро перевести дробь в периодическую, нужно получить знаменатель, состоящий из набора 9

---
| Кол-во 9 | Множители                                      | Кол-во 9 | Множители                                      |
|----------|------------------------------------------------|----------|------------------------------------------------|
| 1        | $3^2$                                          | 11       | $3^2 \cdot 21649 \cdot 513239$                 |
| 2        | $3^2 \cdot 11$                                 | 12       | $3^3 \cdot 7 \cdot 11 \cdot 13 \cdot 37 \cdot 101 \cdot 9901$ |
| 3        | $3^3 \cdot 37$                                 | 13       | $3^2 \cdot 53 \cdot 79 \cdot 265371653$        |
| 4        | $3^2 \cdot 11 \cdot 101$                       | 14       | $3^2 \cdot 11 \cdot 41 \cdot 271 \cdot 9091$   |
| 5        | $3^2 \cdot 41 \cdot 247$                       | 15       | $3^4 \cdot 37 \cdot 333667$                     |
| 6        | $3^3 \cdot 7 \cdot 11 \cdot 13 \cdot 37$        | 16       | $3^2 \cdot 11 \cdot 73 \cdot 101 \cdot 137$     |
| 7        | $3^2 \cdot 239 \cdot 4649$                     | 17       | $3^2 \cdot 11 \cdot 41 \cdot 271 \cdot 9091$   |
| 8        | $3^2 \cdot 11 \cdot 73 \cdot 101 \cdot 137$     | 18       | $3^4 \cdot 37 \cdot 333667$                     |
| 9        | $3^4 \cdot 37 \cdot 333667$                     | 19       | $3^2 \cdot 11 \cdot 41 \cdot 271 \cdot 9091$   |
| 10       | $3^2 \cdot 11 \cdot 41 \cdot 271 \cdot 9091$   | 20       | $3^4 \cdot 37 \cdot 333667$                     |
---
Мне надо перевести $\frac{5}{13}$ в периодический вид. Я ищу ближайшее количество 9, где среди множителей присутствует 13. Это $999999$.
Привожу к виду:
$\frac{5\cdot76923}{13\cdot76923}=\frac{384615}{999999}$. Теперь я значение из числителя могу подставить в повторяющуюся часть
$\frac{5}{13}=0.(384615)$

---
Появляется небольшой парадокс, я покажу его на примере дроби $\frac{1}{6}$. $\frac{1}{3\cdot2}$, но 2 (как и 5) нигде в ряде не встречается. В таком случае можно домножить все на 5 (в случае с 5 на 2) И получиться 10.
$\frac{1\cdot5}{6\cdot5}=\frac{5}{3\cdot 10}=\frac{15}{9\cdot10}=\frac{15}{9}\cdot\frac{1}{10}=1.(6)\cdot\frac{1}{10}$
Деление на 10 это все равно, что сдвинуть точку на 1 цифру влево, и тогда получается что $\frac{1}{6}=0.1(6)$
## Арифметика
### Сложение и вычитание (они схожи)
**Периодическая дробь с обычной**
Пусть будут такие числа: $1.(63)$ и $1.351$
Значение $63$ мы можем спокойно достать, чтобы неповторяющаяся часть была одной длины $1.636(36)+1.351$
Теперь эти части можно сложить
$1.636(36)+1.351=2.987(36)$
**Оба периодические**
Тут будет уже труднее, Я возьму числа $2.7(18)$ и $3.(142)$
Приведем неповторяющуюся часть к одной длине
$2.7(18)+3.1(421)$
Теперь можно периодические части расширить до одной длины, а именно НОД от их длин. Тогда я расширю все до 6
$2.7(18)+3.1(421)=2.7(181818)+3.1(421421)$
Теперь можно сложить периоды, не забывая переносить разряды
$181818+421421=603235$
Тогда $2.7(18)+3.(142)=5.8(603235)$
### Умножение
Для примера я возьму числа $1.(2)$ и $3.(4)$, а потом построю формулу
$1.(2)\cdot3.(4)=\frac{11}{9}\cdot\frac{31}{9}=\frac{341}{81}=\frac{341}{3^4}=4\frac{17}{3^4}$
Ближайший набор находится на месте $999999999$.
$4\frac{17\cdot12345679}{81\cdot12345679}=4\frac{209876543}{999999999}=4.(209876543)$
$\overline{a.(b)}\cdot\overline{c.(d)}=\frac{9a+b}{9}\cdot\frac{9c+d}{9}=\frac{81ac+9ad+9bc+bd}{81}=ac+\frac{9(ad+bc)+bd}{81}=ac+\frac{111111111(ad+bc)+12345679bd}{999999999}=ac+\overline{0.(111111111\cdot(a\cdot d+b\cdot c)+12345679\cdot(b\cdot d))}$
### Деление
$\frac{3.(4)}{1.(2)}=\frac{31}{9}/\frac{11}{9}=\frac{31}{\cancel{9}}\cdot\frac{\cancel{9}}{11}=\frac{31}{11}=\frac{279}{99}=2\frac{81}{99}=2.(81)$
Тут простой алгоритм построить не получится поэтому можно просто переводить в дроби и оперировать с ними

## Заключение
Периодические числа тоже очень интересны, но из-за своей природы трудны для понимания и операций с ними.