- [«Арифметичні оператори](language.operators.arithmetic.md)
- [Побітові оператори »](language.operators.bitwise.md)

- [PHP Manual](index.md)
- [Оператори](language.operators.md)
- оператор привласнення

## Оператор привласнення

Базовий оператор присвоювання позначається як "=". На перший погляд
може здатися, що це оператор "рівно". Насправді, це не так. В
насправді оператор присвоювання означає, що лівий операнд
отримує значення правого вираження, (тобто встановлюється
значенням).

Результатом виконання оператора присвоєння є саме привласнене
значення. Таким чином, результат виконання "$a = 3" буде дорівнювати 3.
Це дозволяє робити трюки на кшталт:

`<?php$a = ($b = 4) + 5; // $a тепер рівно 9, а $b було присвоєно 4.?> `

На додаток до базового оператора присвоювання є "комбіновані
оператори" для всіх [бінарних арифметичних](language.operators.md)
операцій, операцій об'єднання масивів та рядкових операцій, які
дозволяють використовувати деяке значення у виразі, а потім
встановити його як результат цього виразу. Наприклад:

`<?php$a = 3;$a += 5; // встановлює $a в 8, як якщо би ми написали: $a = $a + 5;$b = "Привіт";$b .= "-привіт!"; // встановлює $b в "Привіт-привіт!",  як і $b = $b . "-привіт!";?> `

Зверніть увагу, що присвоєння копіює оригінальну змінну в
нову (привласнення за значенням), таким чином усі наступні зміни
однієї зі змінних ніяк не позначаться на іншій. Це також слід
враховувати, якщо вам треба скопіювати щось типу великого масиву
довгому циклі.

Винятком із звичайного для PHP способу привласнення за значенням
є об'єкти (object), які присвоюються за посиланням.
Примусово скопіювати об'єкти за значенням можна за допомогою
спеціального ключового слова [clone](language.oop5.cloning.md).

### Привласнення за посиланням

Присвоєння посилання також підтримується, для нього використовується
синтаксис $var = &$othervar;. Привласнення за посиланням означає, що обидві
змінні вказують на одні й ті самі дані та жодного копіювання не
відбувається.

**Приклад #1 Привласнення за посиланням**

` <?php$a = 3;$b = &$a; // $b - це посилання на $aprint "$a
"; // друкує 3print "$b
"; // друкує 3$a = 4; // міняємо $aprint "$a
"; // друкує 4print "$b
"; // також друкує 4, так як $b є посиланням на $a,               // а значення змінної $a 

Оператор [new](language.oop5.basic.md#language.oop5.basic.new)
автоматично повертає посилання, тому присвоєння результату операції
[new](language.oop5.basic.md#language.oop5.basic.new) за посиланням
є помилкою.

` <?phpclass C {}$o = &new C;?> `

Результат виконання цього прикладу:

Parse error: syntax error, unexpected 'new' (T_NEW) in …

Для отримання більш повної інформації про посилання та їх можливості
Зверніться до розділу [Докладніше про посилання](language.references.md).

### Оператори арифметичного присвоєння

| приклад     | Еквівалент Операція |                     |
|-------------|---------------------|---------------------|
| $a += $b    | $a = $a + $b        | Додавання           |
| $a -= $b    | $a = $a - $b        | Віднімання          |
| $a \*= $b   | $a = $a \* $b       | Розмноження         |
| $a /= $b    | $a = $a / $b        | Поділ               |
| $a %= $b    | $a = $a % $b        | Модуль              |
| $a \*\*= $b | $a = $a \*\* $b     | Зведення на ступінь |

### Оператори побитового привласнення

| приклад     | Еквівалент Операція |                                |
|-------------|---------------------|--------------------------------|
| $a &= $b    | $a = $a & $b        | Побітове І                     |
| $a \|= $b   | $a = $a \| $b       | Побітове АБО                   |
| $a^=$b      | $a = $a^$b          | Побітове що виключає АБО (Xor) |
| $a \<\<= $b | $a = $a \<\< $b     | Побітове зрушення вліво        |
| $a \>\>= $b | $a = $a \>\> $b     | Побітове зрушення вправо       |

### Інші оператори привласнення

| приклад   | Еквівалент Операція |                     |
|-----------|---------------------|---------------------|
| $a.=$b    | $a = $a. $b         | Конкатенація рядків |
| $a ??= $b | $a = $a ?? $b       | Поєднання з Null    |

### Дивіться також

- [арифметичні оператори](language.operators.arithmetic.md)
- [побітові оператори](language.operators.bitwise.md)
- [оператори об'єднання з null](language.operators.comparison.md#language.operators.comparison.coalesce)
