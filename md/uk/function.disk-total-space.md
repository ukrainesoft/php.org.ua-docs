---
navigation:
  - function.disk-free-space.md: « disk\_free\_space
  - function.diskfreespace.md: diskfreespace »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: disk\_total\_space
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# disk\_total\_space

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

disk\_total\_space — Повертає загальний розмір файлової системи або розділу диска

### Опис

```methodsynopsis
disk_total_space(string $directory): float|false
```

Функція повертає загальний розмір у байтах вказаного розділу диска чи каталогу.

### Список параметрів

`directory`

Директорія файлової системи чи розділ диска.

### Значення, що повертаються

Повертає загальний розмір у байтах у вигляді числа з плаваючою точкою або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**disk\_total\_space()\*\*\*\*

```php
<?php
// $df содержит общий размер диска "/" в байтах
$ds = disk_total_space("/");

// В Windows:
$ds = disk_total_space("C:");
$ds = disk_total_space("D:");
?>
```

### Примітки

> **Зауваження**: Ця функція не застосовується для роботи з [віддаленими файлами](features.remote-files.md)оскільки файл повинен бути доступний через файлову систему сервера.

### Дивіться також

-   [disk\_free\_space()](function.disk-free-space.md) \- Повертає розмір доступного простору в каталозі чи файловій системі
