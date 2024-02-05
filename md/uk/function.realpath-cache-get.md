---
navigation:
  - function.readlink.md: « readlink
  - function.realpath-cache-size.md: realpath\_cache\_size »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: realpath\_cache\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# realpath\_cache\_get

(PHP 5 >= 5.3.2, PHP 7, PHP 8)

realpath\_cache\_get — Отримує записи з кеша realpath

### Опис

```methodsynopsis
realpath_cache_get(): array
```

Отримує вміст кешу реального шляху.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив записів із кеша realpath. Ключі є записами realpath, а значення є масивами даних, що містять обчислений шлях, час життя кеша та інших даних, що зберігаються у кеші.

### Приклади

**Пример #1 Пример использования**realpath\_cache\_get()\*\*\*\*

```php
<?php
var_dump(realpath_cache_get());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(2) {
  ["/test"] => array(4) {
    ["key"] => int(123456789)
    ["is_dir"] => bool(true)
    ["realpath"] => string(5) "/test"
    ["expires"] => int(1260318939)
  }
  ["/test/test.php"] => array(4) {
    ["key"] => int(987654321)
    ["is_dir"] => bool(false)
    ["realpath"] => string(12) "/root/test.php"
    ["expires"] => int(1260318939)
  }
}
```

### Дивіться також

-   [realpath\_cache\_size()](function.realpath-cache-size.md) \- Отримує розмір кеша realpath
