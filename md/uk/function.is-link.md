---
navigation:
  - function.is-file.md: « is\_file
  - function.is-readable.md: is\_readable »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: is\_link
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_link

(PHP 4, PHP 5, PHP 7, PHP 8)

is\_link — Визначає, чи є файл символічним посиланням

### Опис

```methodsynopsis
is_link(string $filename): bool
```

Визначає, чи є файл символічним посиланням.

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо файл існує і є символічним посиланням, інакше повертає **`false`**

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Створюємо файл та підтверджуємо, що він є символічним посиланням**

```php
<?php
$link = 'uploads';

if (is_link($link)) {
    echo readlink($link);
} else {
    symlink('uploads.php', $link);
}
?>
```

### Примітки

> **Зауваження**: Результати цієї функції кешуються Більш детальну інформацію дивіться у розділі [clearstatcache()](function.clearstatcache.md)

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з *деякими* обгортками url. Список обгорток, що підтримуються сімейством функцій [stat()](function.stat.md), смотрите в разделе[Підтримувані протоколи та обгортки](wrappers.md)

### Дивіться також

-   [is\_dir()](function.is-dir.md) \- Визначає, чи є ім'я файлу директорією
-   [is\_file()](function.is-file.md) \- Визначає, чи файл є звичайним файлом
-   [readlink()](function.readlink.md) \- Повертає файл, на який вказує символічне посилання
