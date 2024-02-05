---
navigation:
  - function.stat.md: « stat
  - function.tempnam.md: tempnam »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: symlink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# symlink

(PHP 4, PHP 5, PHP 7, PHP 8)

symlink — Створює символічне посилання

### Опис

```methodsynopsis
symlink(string $target, string $link): bool
```

**symlink()** створює символічне посилання на існуючий файл `target`с именем`link`

### Список параметрів

`target`

Ціль посилання.

`link`

Ім'я посилання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Функція завершується з помилкою та видає **`E_WARNING`**, якщо `link` вже існує. У Windows функція також не працює та видає **`E_WARNING`**, якщо `target` не існує.

### Приклади

**Приклад #1 Створення символічного посилання**

```php
<?php
$target = 'uploads.php';
$link = 'uploads';
symlink($target, $link);

echo readlink($link);
?>
```

### Дивіться також

-   [link()](function.link.md) \- Створює жорстке посилання
-   [readlink()](function.readlink.md) \- Повертає файл, на який вказує символічне посилання
-   [linkinfo()](function.linkinfo.md) \- Повертає інформацію про посилання
-   [unlink()](function.unlink.md) \- Видаляє файл
