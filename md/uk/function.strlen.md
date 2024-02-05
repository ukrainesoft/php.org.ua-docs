---
navigation:
  - function.stristr.md: « stristr
  - function.strnatcasecmp.md: strnatcasecmp »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strlen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strlen

(PHP 4, PHP 5, PHP 7, PHP 8)

strlen — Повертає довжину рядка

### Опис

```methodsynopsis
strlen(string $string): int
```

Повертає довжину рядка `string`

### Список параметрів

`string`

Рядок (string), на яку вимірюється довжина.

### Значення, що повертаються

Функція повертає довжину рядка `string`в байтах.

### Приклади

**Приклад #1 Приклад використання** strlen()\*\*\*\*

```php
<?php
$str = 'abcdef';
echo strlen($str); // 6

$str = ' ab cd ';
echo strlen($str); // 7
?>
```

### Примітки

> **Зауваження** :
> 
> Функция**strlen()** поверне кількість байт, а не кількість символів у рядку.

### Дивіться також

-   [count()](function.count.md) \- Підраховує кількість елементів масиву або Countable об'єкті
-   [grapheme\_strlen()](function.grapheme-strlen.md) \- отримує довжину рядка в одиницях графеми
-   [iconv\_strlen()](function.iconv-strlen.md) \- Повертає кількість символів у рядку
-   [mb\_strlen()](function.mb-strlen.md) \- Отримує довжину рядка
