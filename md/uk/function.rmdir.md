---
navigation:
  - function.rewind.md: « rewind
  - function.set-file-buffer.md: set\_file\_buffer »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: rmdir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rmdir

(PHP 4, PHP 5, PHP 7, PHP 8)

rmdir - Видаляє директорію

### Опис

```methodsynopsis
rmdir(string $directory, ?resource $context = null): bool
```

Намагається видалити директорію з ім'ям `directory`. Директорія має бути порожньою і повинні мати необхідні для цього права. При невдалому виконанні буде згенеровано помилку рівня **`E_WARNING`**

### Список параметрів

`directory`

Шлях до директорії.

`context`

Ресурс (resource) с[контекстом потоку](stream.contexts.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** rmdir()\*\*\*\*

```php
<?php
if (!is_dir('examples')) {
    mkdir('examples');
}

rmdir('examples');
?>
```

### Дивіться також

-   [is\_dir()](function.is-dir.md) \- Визначає, чи є ім'я файлу директорією
-   [mkdir()](function.mkdir.md) \- створює директорію
-   [unlink()](function.unlink.md) \- Видаляє файл
