---
navigation:
  - function.gzread.md: « gzread
  - function.gzseek.md: gzseek »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzrewind
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gzrewind

(PHP 4, PHP 5, PHP 7, PHP 8)

gzrewind — Перемістити вказівник gz-файлу на початок

### Опис

```methodsynopsis
gzrewind(resource $stream): bool
```

Встановлює вказівник на позицію файлу початку потоку цього файла.

### Список параметрів

`stream`

Вказівник на gz-файл, повернутий після його успішного відкриття функцією [gzopen()](function.gzopen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [gzseek()](function.gzseek.md) \- Перемістити вказівник на позицію в покажчику gz-файлу
-   [gztell()](function.gztell.md) \- Повертає поточну позицію читання/запису в покажчику gz-файлу
