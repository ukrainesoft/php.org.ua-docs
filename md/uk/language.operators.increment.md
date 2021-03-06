- [« Оператори виконання](language.operators.execution.md)
- [Логічні оператори »](language.operators.logical.md)

- [PHP Manual](index.md)
- [Оператори](language.operators.md)
- Оператори інкременту та декременту

## Оператори інкременту та декременту

PHP підтримує префіксні та постфіксні оператори інкременту та
декременту у стилі C.

> **Примітка**: Оператори інкременту/декременту впливають лише на числа
> та рядки. Масиви, об'єкти, булеві значення та ресурси не будуть
> Змінено. Декремент **`null`** також не дасть жодного ефекту, проте
> інкремент надасть значення `1`.

| приклад | Назва                                                                     | Дія                                                |
| ------- | ------------------------------------------------------------------------- | -------------------------------------------------- |
| ++$a    | Префіксний інкремент Збільшує $a на одиницю, потім повертає значення $a.  |                                                    |
| $a++    | Постфіксний інкремент Повертає значення $a, потім збільшує $a на одиницю. |                                                    |
| --$a    | Префіксний декремент                                                      | Зменшує $a на одиницю, потім повертає значення $a. |
| $a--    | Постфіксний декремент Повертає значення $a, потім зменшує $a на одиницю.  |                                                    |

**Оператори інкременту та декременту**

Наведемо приклад простого скрипту:

` <?phpecho "<h3>Постфіксний інкремент</h3>";$a = 5;echo "Має бути 5: " . $a++. "<br />
";echo "Має бути 6: " . $a . "<br />
";echo "<h3>Префіксний інкремент</h3>";$a = 5;echo "Має бути 6: " . ++$a . "<br />
";echo "Має бути 6: " . $a . "<br />
";echo "<h3>Постфіксний декремент</h3>";$a = 5;echo "Має бути 5: " . $a-- . "<br />
";echo "Має бути 4: " . $a . "<br />
";echo "<h3>Префіксний декремент</h3>";$a = 5;echo "Має бути 4: " . --$a . "<br />
";echo "Має бути 4: " . $a . "<br />
";?> `

PHP слідує угодам Perl (на відміну від С) щодо виконання
арифметичних операцій із символьними змінними. Наприклад, у PHP та
Perl `$a = 'Z'; $a++;` надасть `$a` значення `'AA'`, тоді як у C
`a = 'Z'; a++;` привласнить `a` значення ``['` (ASCII-значення ``Z'` одно
90, а ASCII-значення "["" дорівнює 91). Слід врахувати, що до символьних
змінним можна застосовувати операцію інкременту, тоді як операцію
декременту застосовувати не можна, крім того, підтримуються лише
ASCII-символи (a-z та A-Z). Спроба інкременту/декременту інших
символьних змінних не матиме жодного ефекту, вихідний рядок
залишиться незмінною.

**Приклад #1 Арифметичні операції із символьними змінними**

`<?phpecho '== Букви ==' . PHP_EOL;$s = 'W';for ($n=0; $n<6; $n++) {   echo ++$s . PHP_EOL;}// З цифрами кілька по іншомуecho '== Цифри ==' . PHP_EOL;$d = 'A8';for ($n=0;$n<6; $n++) {   echo ++$d . PHP_EOL;}$d = 'A08';for ($n=0; $n<6; $n++) {   echo ++$d . PHP_EOL;}?> `

Результат виконання цього прикладу:

== Літери ==
X
Y
Z
AA
AB
AC
== Цифри ==
A9
B0
B1
B2
B3
B4
A09
A10
A11
A12
A13
A14

Інкрементування або декрементування булевих змінних не призводить
до жодного результату.
