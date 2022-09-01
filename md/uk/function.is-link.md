---
navigation:
  - function.is-file.html: « isfile
  - function.is-readable.html: ісreadable »
  - index.html: PHP Manual
  - ref.filesystem.html: Функції файлової системи
title: ісlink
---
# ісlink

(PHP 4, PHP 5, PHP 7, PHP 8)

ісlink — Визначає, чи є файл символічним посиланням

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
$link = 'uploads';

if (is_link($link)) {
    echo(readlink($link));
} else {
    symlink('uploads.php', $link);
}
?>
```

### Примітки

> **Зауваження**: Результати цієї функції кешуються Більш детальну інформацію дивіться у розділі [clearstatcache()](function.clearstatcache.html)

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з *деякими* обгортками url. Список обгорток, що підтримуються сімейством функцій [stat()](function.stat.html), дивіться у розділі [Підтримувані протоколи та обгортки](wrappers.html)

### Дивіться також

-   [ісdir()](function.is-dir.html) - Визначає, чи є ім'я файлу директорією
-   [ісfile()](function.is-file.html) - Визначає, чи файл є звичайним файлом
-   [readlink()](function.readlink.html) - Повертає файл, на який вказує символічне посилання
