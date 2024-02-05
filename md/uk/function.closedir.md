---
navigation:
  - function.chroot.md: « chroot
  - function.dir.md: dir »
  - index.md: PHP Manual
  - ref.dir.md: Функції для роботи з каталогами
title: closedir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# closedir

(PHP 4, PHP 5, PHP 7, PHP 8)

closedir — Закриває дескриптор каталогу

### Опис

```methodsynopsis
closedir(?resource $dir_handle = null): void
```

Закриває потік, пов'язаний з каталогом і переданий як параметр `dir_handle`. Перед використанням цієї функції потік повинен бути відкритий за допомогою функції [opendir()](function.opendir.md)

### Список параметрів

`dir_handle`

Дескриптор каталогу (resource), раніше відкритий за допомогою [opendir()](function.opendir.md). Якщо дескриптор каталогу не вказано, використовується останній дескриптор, відкритий функцією [opendir()](function.opendir.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**closedir()\*\*\*\*

```php
<?php
$dir = "/etc/php5/";

// Открываем известную директорию, читаем её в переменную и закрываем
if (is_dir($dir)) {
    if ($dh = opendir($dir)) {
        $directory = readdir($dh);
        closedir($dh);
    }
}
?>
```
