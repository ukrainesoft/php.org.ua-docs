---
navigation:
  - function.lchown.html: « lchown
  - function.linkinfo.html: linkinfo »
  - index.html: PHP Manual
  - ref.filesystem.html: Функції файлової системи
title: link
---
# link

(PHP 4, PHP 5, PHP 7, PHP 8)

link — Створює жорстке посилання

### Опис

```methodsynopsis
link(string $target, string $link): bool
```

**link()** створює жорстке заслання.

### Список параметрів

`target`

Ціль посилання.

`link`

Ім'я посилання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Функція завершується з помилкою та видає **`E_WARNING`**, якщо `link` вже існує або якщо `target` не існує.

### Приклади

**Приклад #1 Створення простого жорсткого посилання**

```php
<?php
$target = 'source.ext'; // Это уже существующий файл
$link = 'newfile.ext'; // Это файл, который вы хотите привязать к первому

link($target, $link);
?>
```

### Примітки

> **Зауваження**: Ця функція не застосовується для роботи з [віддаленими файлами](features.remote-files.html)оскільки файл повинен бути доступний через файлову систему сервера.

> **Зауваження**: Тільки для Windows: Для цієї функції необхідно, щоб PHP був запущений у привілейованому режимі або з вимкненим UAC.

### Дивіться також

-   [symlink()](function.symlink.html) - Створює символічне посилання
-   [readlink()](function.readlink.html) - Повертає файл, на який вказує символічне посилання
-   [linkinfo()](function.linkinfo.html) - Повертає інформацію про посилання
-   [unlink()](function.unlink.html) - Видаляє файл
