---
navigation:
  - function.pack.md: « pack
  - function.sapi-windows-cp-conv.md: sapi\_windows\_cp\_conv »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: php\_strip\_whitespace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# php\_strip\_whitespace

(PHP 5, PHP 7, PHP 8)

php\_strip\_whitespace — Повертає вихідний код без коментарів та пробілів

### Опис

```methodsynopsis
php_strip_whitespace(string $filename): string
```

Повертає вихідний код PHP у файл (`filename`) з віддаленими коментарями та пробілами. Ця функція може бути корисною для визначення фактичного обсягу чистого коду у скриптах порівняно з кількістю коментарів. Функція аналогічна використанню **php -w**из[командного рядка](features.commandline.md)

### Список параметрів

`filename`

Шлях до PHP-файлу.

### Значення, що повертаються

Повертає очищений вихідний код у разі успішного виконання або порожній рядок у разі помилки.

> **Зауваження** :
> 
> Ця функція бере до уваги значення INI-директиви [short\_open\_tag](ini.core.md#ini.short-open-tag)

### Приклади

**Приклад #1 Приклад використання** php\_strip\_whitespace()\*\*\*\*

```php
<?php
// PHP комментарий

/*
 * Другой PHP комментарий
 */

echo        php_strip_whitespace(__FILE__);
// Символы новой строки считаются пробелами, и также удаляются:
do_nothing();
?>
```

Результат виконання наведеного прикладу:

```
<?php
 echo php_strip_whitespace(__FILE__); do_nothing(); ?>
```

В результаті виконання прикладу виведено вихідний код PHP без коментарів, прогалин та порожніх рядків.
