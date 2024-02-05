---
navigation:
  - function.strtok.md: « strtok
  - function.strtoupper.md: strtoupper »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strtolower
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strtolower

(PHP 4, PHP 5, PHP 7, PHP 8)

strtolower — Перетворює рядок на нижній регістр

### Опис

```methodsynopsis
strtolower(string $string): string
```

Повертає рядок `string`, де всі буквені символи ASCII переведені в нижній регістр.

Байти в діапазоні від `"A"`(0x41) до`"Z"` (0x5a) будуть перетворені у відповідну малу літеру шляхом додавання 32 до кожного значення байта.

Функцію можна використовувати для перетворення символів ASCII у рядках, закодованих у UTF-8, оскільки багатобайтові символи UTF-8 будуть проігноровані. Для перетворення багатобайтових не ASCII символів використовуйте функцію [mb\_strtolower()](function.mb-strtolower.md)

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає рядок у нижньому регістрі.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Перетворення регістру більше не залежить від локалі, встановленої за допомогою функції [setlocale()](function.setlocale.md). . Буде перетворено лише символи ASCII. |

### Приклади

**Пример #1 Пример использования**strtolower()\*\*\*\*

```php
<?php
$str = "Mary Had A Little Lamb and She LOVED It So";
$str = strtolower($str);
echo $str; // выводит: mary had a little lamb and she loved it so
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [strtoupper()](function.strtoupper.md) \- Перетворює рядок у верхній регістр
-   [ucfirst()](function.ucfirst.md) \- Перетворює перший символ рядка у верхній регістр
-   [ucwords()](function.ucwords.md) \- Перетворює у верхній регістр перший символ кожного слова у рядку
-   [mb\_strtolower()](function.mb-strtolower.md) \- Наводить рядок до нижнього регістру
