---
navigation:
  - function.lcfirst.md: « lcfirst
  - function.localeconv.md: localeconv »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: levenshtein
---
# levenshtein

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

levenshtein — Обчислює відстань Левенштейна між двома рядками

### Опис

```methodsynopsis
levenshtein(    string $string1,    string $string2,    int $insertion_cost = 1,    int $replacement_cost = 1,    int $deletion_cost = 1): int
```

Відстань Левенштейна - це мінімальна кількість вставок, замін та видалень символів, необхідна для перетворення `string1` в `string2`. Складність алгоритму дорівнює `O(m*n)`, де `n` і `m` - Довжини рядків `string1` і `string2` (Непогано в порівнянні з [similartext()](function.similar-text.html), що має складність `O(max(n,m)**3)`, Але все ж таки досить багато).

Якщо `insertion_cost` `replacement_cost` та/або `deletion_cost` не рівні `1`алгоритм адаптується для вибору найдешевших перетворень. Наприклад. якщо `$insertion_cost + $deletion_cost < $replacement_cost`, заміни не будуть виконуватися, натомість будуть виконуватися вставки та видалення.

### Список параметрів

`string1`

Один із рядків, для яких обчислюється відстань Левенштейна.

`string2`

Один із рядків, для яких обчислюється відстань Левенштейна.

`insertion_cost`

Визначає вартість вставки.

`replacement_cost`

Визначає вартість заміни.

`deletion_cost`

Визначає вартість видалення.

### Значення, що повертаються

Ця функція повертає відстань Левенштейна між двома рядками, або -1, якщо хоча б один із рядків довший за 255 символів.

### список змін

| Версия | Описание |
| --- | --- |
|  | До цієї версії **levenshtein()** треба було викликати із двома чи п'ятьма аргументами. |

### Приклади

**Приклад #1 Приклад використання **levenshtein()****

```php
<?php
// введённое слово с опечаткой
$input = 'carrrot';

// Масив сверяемых слов
$words  = array('apple','pineapple','banana','orange',
                'radish','carrot','pea','bean','potato');

// кратчайшее расстояние пока ещё не найдено
$shortest = -1;

// проходим по словам для нахождения самого близкого варианта
foreach ($words as $word) {

    // вычисляем расстояние между входным словом и текущим
    $lev = levenshtein($input, $word);

    // проверяем полное совпадение
    if ($lev == 0) {

        // это ближайшее слово (точное совпадение)
        $closest = $word;
        $shortest = 0;

        // выходим из цикла - мы нашли точное совпадение
        break;
    }

    // если это расстояние меньше следующего наименьшего расстояния
    // ИЛИ если следующее самое короткое слово ещё не было найдено
    if ($lev <= $shortest || $shortest < 0) {
        // устанивливаем ближайшее совпадение и кратчайшее расстояние
        $closest  = $word;
        $shortest = $lev;
    }
}

echo "Вы ввели: $input\n";
if ($shortest == 0) {
    echo "Найдено точное совпадение: $closest\n";
} else {
    echo "Вы не имели в виду: $closest?\n";
}

?>
```

Результат виконання цього прикладу:

```
Вы ввели: carrrot
Вы не имели в виду: carrot?
```

### Дивіться також

-   [soundex()](function.soundex.md) - Повертає ключ soundex для рядка
-   [similartext()](function.similar-text.html) - обчислює ступінь схожості двох рядків
-   [metaphone()](function.metaphone.md) - Повертає ключ metaphone для рядка
