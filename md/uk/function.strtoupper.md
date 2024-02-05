---
navigation:
  - function.strtolower.md: « strtolower
  - function.strtr.md: strtr »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strtoupper
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strtoupper

(PHP 4, PHP 5, PHP 7, PHP 8)

strtoupper — Перетворює рядок у верхній регістр

### Опис

```methodsynopsis
strtoupper(string $string): string
```

Повертає рядок `string`, де всі буквені символи ASCII переведені у верхній регістр.

Байти в діапазоні від `"a"`(0x61) до`"z"` (0x7a) будуть перетворені на відповідну заголовну букву шляхом віднімання 32 з кожного значення байта.

Функцію можна використовувати для перетворення символів ASCII у рядках, закодованих у UTF-8, оскільки багатобайтові символи UTF-8 будуть проігноровані. Для перетворення багатобайтових не ASCII символів використовуйте функцію [mb\_strtoupper()](function.mb-strtoupper.md)

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає рядок у верхньому регістрі.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Перетворення регістру більше не залежить від локалі, встановленої за допомогою функції [setlocale()](function.setlocale.md). . Буде перетворено лише символи ASCII. |

### Приклади

**Приклад #1 Приклад використання** strtoupper()\*\*\*\*

```php
<?php
$str = "Mary Had A Little Lamb and She LOVED It So";
$str = strtoupper($str);
echo $str; // выводит: MARY HAD A LITTLE LAMB AND SHE LOVED IT SO
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [strtolower()](function.strtolower.md) \- Перетворює рядок на нижній регістр
-   [ucfirst()](function.ucfirst.md) \- Перетворює перший символ рядка у верхній регістр
-   [ucwords()](function.ucwords.md) \- Перетворює у верхній регістр перший символ кожного слова у рядку
-   [mb\_strtoupper()](function.mb-strtoupper.md) \- Приведе рядок до верхнього регістру
