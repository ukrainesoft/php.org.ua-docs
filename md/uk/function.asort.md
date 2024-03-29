---
navigation:
  - function.arsort.md: « arsort
  - function.compact.md: compact »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: asort
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# asort

(PHP 4, PHP 5, PHP 7, PHP 8)

asort — Сортує масив у порядку зростання, зберігаючи асоціацію індексів

### Опис

```methodsynopsis
asort(array &$array, int $flags = SORT_REGULAR): true
```

Сортує масив (`array`) у порядку зростання так, щоб ключі масиву зберігали кореляцію зі значеннями, з якими вони пов'язані.

Функцією користуються для сортування асоціативних масивів, котрим важливий поточний порядок елементів.

> **Зауваження** :
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

> **Зауваження** :
> 
> Скидає внутрішній покажчик масиву перший елемент.

### Список параметрів

`array`

Вхідний масив

`flags`

Необов'язковий другий параметр `flags` змінює поведінку сортування і може набувати таких значень:

Прапори типів сортування:

-   \*\*`SORT_REGULAR`\*\*- Звичайне порівняння елементів; подробиці описані в розділі[оператори порівняння](language.operators.comparison.md)
-   \*\*`SORT_NUMERIC`\*\*- Чисельне порівняння елементів
-   \*\*`SORT_STRING`\*\*- рядкове порівняння елементів
-   \*\*`SORT_LOCALE_STRING`\*\*— Порівняти елементи як рядки на основі поточного мовного стандарту. Прапор використовує мовний стандарт, який можна змінити функцією[setlocale()](function.setlocale.md)
-   **`SORT_NATURAL`** - Порівняння елементів як рядки, використовуючи "природний порядок", наприклад [natsort()](function.natsort.md)
-   \*\*`SORT_FLAG_CASE`**\- можна об'єднувати (побітове АБО) з**`SORT_STRING`** або **`SORT_NATURAL`\*\*для сортування рядків без урахування регістру

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Приклади

**Приклад #1 Приклад використання функції** asort()\*\*\*\*

```php
<?php

$fruits = array("d" => "лимон", "a" => "апельсин", "b" => "банан", "c" => "яблоко");
asort($fruits);
foreach ($fruits as $key => $val) {
    echo "$key = $val\n";
}
?>
```

Результат виконання наведеного прикладу:

```
c = яблоко
b = банан
d = лимон
a = апельсин
```

Назви фруктів були відсортовані в алфавітному порядку та ключі, пов'язані з елементами, були збережені.

### Дивіться також

-   [sort()](function.sort.md) \- Сортує масив за зростанням
-   [arsort()](function.arsort.md) \- Сортує масив у порядку зменшення, зберігаючи асоціацію індексів
-   [Порівняння функцій сортування масивів](array.sorting.md)
