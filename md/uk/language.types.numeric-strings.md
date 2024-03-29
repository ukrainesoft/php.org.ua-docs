---
navigation:
  - language.types.string.md: « Рядки
  - language.types.array.md: Масиви »
  - index.md: PHP Manual
  - language.types.md: Типи
title: Числові рядки
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Числові рядки

У PHP рядок (string) вважається числовим, якщо його можна інтерпретувати як ціле (int) число або число з плаваючою точкою (float).

Формально з PHP 8.0.0:

```
WHITESPACES      \s*
LNUM             [0-9]+
DNUM             ([0-9]*[\.]{LNUM}) | ({LNUM}[\.][0-9]*)
EXPONENT_DNUM    (({LNUM} | {DNUM}) [eE][+-]? {LNUM})
INT_NUM_STRING   {WHITESPACES} [+-]? {LNUM} {WHITESPACES}
FLOAT_NUM_STRING {WHITESPACES} [+-]? ({DNUM} | {EXPONENT_DNUM}) {WHITESPACES}
NUM_STRING       ({INT_NUM_STRING} | {FLOAT_NUM_STRING})
```

У PHP також є концепція *префіксною* числового рядка. Це рядок, який починається як числовий і продовжується будь-якими іншими символами.

> **Зауваження** :
> 
> Будь-який рядок, що містить букву `E` (без урахування регістру), обмежену цифрами, сприйматиметься як число, виражене у науковій нотації. Це може призвести до несподіваних результатів.
> 
> ```php
> <?php
> 
> var_dump("0D1" == "000"); // false, "0D1" - не наукова нотація
> var_dump("0E1" == "000"); // true, "0E1" - це 0 * (10 ^ 1) або 0
> var_dump("2E1" == "020"); // true, "2E1" - це 2 * (10 ^ 1) або 20
> ?>
> ```

### Рядки, що використовуються в числових контекстах

Коли рядок необхідно використовувати як число (наприклад арифметичні операції, декларація цілого чисельного типу, і т. д.), використовується наступний алгоритм дій:

1.  Якщо рядок числовий, представляє ціле число і не перевищує максимально допустимого значення для типу int (визначеного в\*\*`PHP_INT_MAX`\*\*), вона наводиться до типу int. Інакше вона наводиться до типу float.
2.  Якщо в заданому контексті можна використовувати префіксний числовий рядок, то, якщо початок рядка представляє ціле число і не перевищує максимально допустимого значення для типу int (визначеного в\*\*`PHP_INT_MAX`**), вона наводиться до типу int. Інакше вона наводиться до типу float. Також, у цьому випадку, видається помилка рівня**`E_WARNING`\*\*
3.  Якщо рядок не числовий - викидається виняток[TypeError](class.typeerror.md)

### Поведінка до PHP 8.0.0

До PHP 8.0.0 рядок вважався числовим лише у випадку, якщо він *починалася* із пробілових символів. Якщо вона *завершувалася* пробельними символами - вона вважалася префіксною числовою.

До PHP 8.0.0, коли рядок необхідно використовувати як число, використовувався той же алгоритм, що описаний вище, але з деякими відмінностями:

-   Використання префіксного числового рядка викликало помилку рівня\*\*`E_NOTICE`**, а не**`E_WARNING`\*\*
-   Якщо рядок не був числовим, викликалася помилка рівня\*\*`E_WARNING`\*\*, а сам рядок приводився до

До PHP 7.1.0 не викликалася помилка рівня **`E_NOTICE`**, ни\*\*`E_WARNING`\*\*

```php
<?php
$foo = 1 + "10.5";                // $foo — число с плавающей точкой (11.5)
$foo = 1 + "-1.3e3";              // $foo — число с плавающей точкой (-1299)
$foo = 1 + "bob-1.3e3";           // TypeError начиная с PHP 8.0.0. Ранее $foo принималось за целое число (1)
$foo = 1 + "bob3";                // TypeError начиная с PHP 8.0.0, Ранее $foo принималось за целое число (1)
$foo = 1 + "10 Small Pigs";       // $foo — целое (11). В PHP 8.0.0 выдаётся ошибка уровня E_WARNING, а в более ранних версиях — уровня E_NOTICE
$foo = 4 + "10.2 Little Piggies"; // $foo — число с плавающей точкой (14.2). В PHP 8.0.0 выдаётся ошибка уровня E_WARNING, а в более ранних версиях — уровня E_NOTICE
$foo = "10.0 pigs " + 1;          // $foo — число с плавающей точкой (11). В PHP 8.0.0 выдаётся ошибка уровня E_WARNING, а в более ранних версиях — уровня E_NOTICE
$foo = "10.0 pigs " + 1.0;        // $foo — число с плавающей точкой (11). В PHP 8.0.0 выдаётся ошибка уровня E_WARNING, а в более ранних версиях — уровня E_NOTICE
?>
```
