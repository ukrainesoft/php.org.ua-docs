---
navigation:
  - phar.iswritable.md: '« Phar::isWritable'
  - phar.mapphar.md: 'Phar::mapPhar »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::loadPhar'
---
# Phar::loadPhar

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::loadPhar — Завантажити phar-архів із псевдонімом

### Опис

```methodsynopsis
final public static Phar::loadPhar(string $filename, ?string $alias = null): bool
```

Може використовуватись для завантаження зовнішнього архіву Phar. Те, що для phar-архіву призначається псевдонім, дозволяє надалі використовувати більш короткі посилання для доступу до нього або для завантаження архівів Phar, що містять тільки дані і не призначені для виконання.

### Список параметрів

`filename`

Шлях до завантажуваного phar-архіву

`alias`

Псевдонім для доступу до архіву. Зверніть увагу, що багато phar-архівів мають свій явно заданий псевдонім і, при заданні нового псевдоніма, буде викинуто виняток [PharException](class.pharexception.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Якщо заданий параметр із псевдонімом, а архів, що завантажується, вже має псевдонім, то буде викинуто виняток [PharException](class.pharexception.md)

### Приклади

**Приклад #1 Приклад використання **Phar::loadPhar()****

Phar::loadPhar можна використовувати будь-де, тоді як Phar::mapPhar тільки в завантажувачі (stub) Phar-архіву.

```php
<?php
try {
    Phar::loadPhar('/path/to/phar.phar', 'my.phar');
    echo file_get_contents('phar://my.phar/file.txt');
} catch (PharException $e) {
    echo $e;
}
?>
```

### Дивіться також

-   [Phar::mapPhar()](phar.mapphar.md) - Прочитати поточний запущений phar-архів та зареєструвати його маніфест
