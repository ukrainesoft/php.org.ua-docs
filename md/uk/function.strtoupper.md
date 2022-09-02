---
navigation:
  - function.strtolower.md: « strtolower
  - function.strtr.md: strtr »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strtoupper
---
# strtoupper

(PHP 4, PHP 5, PHP 7, PHP 8)

strtoupper — Перетворює рядок на верхній регістр

### Опис

```methodsynopsis
strtoupper(string $string): string
```

Повертає рядок `string`, де всі літерні символи переведені у верхній регістр.

Приналежність тієї чи іншої символу до буквеним визначається з урахуванням поточної локалі. Це означає, що, наприклад, у локалі "C", що використовується за умовчанням, символ ä не буде перетворений.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає рядок у верхньому регістрі.

### Приклади

**Приклад #1 Приклад використання **strtoupper()****

```php
<?php
$str = "Mary Had A Little Lamb and She LOVED It So";
$str = strtoupper($str);
echo $str; // выводит: MARY HAD A LITTLE LAMB AND SHE LOVED IT SO
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [strtolower()](function.strtolower.md) - Перетворює рядок на нижній регістр
-   [ucfirst()](function.ucfirst.md) - Перетворює перший символ рядка у верхній регістр
-   [ucwords()](function.ucwords.md) - Перетворює на верхній регістр перший символ кожного слова в рядку
-   [мбstrtoupper()](function.mb-strtoupper.md) - Приведення рядка до верхнього регістру
