---
navigation:
  - function.gzseek.md: « gzseek
  - function.gzuncompress.md: gzuncompress »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gztell
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gztell

(PHP 4, PHP 5, PHP 7, PHP 8)

gztell — Повертає поточну позицію читання/запису в покажчику gz-файлу

### Опис

```methodsynopsis
gztell(resource $stream): int|false
```

Отримує позицію покажчика файлу, тобто зміщення потоку розпакованого файлу.

### Список параметрів

`stream`

Вказівник на gz-файл, повернутий після його успішного відкриття функцією [gzopen()](function.gzopen.md)

### Значення, що повертаються

Поточна позиція або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [gzopen()](function.gzopen.md) \- Відкрити gz-файл
-   [gzseek()](function.gzseek.md) \- Перемістити вказівник на позицію в покажчику gz-файлу
-   [gzrewind()](function.gzrewind.md) \- Перемістити позицію покажчик gz-файлу на початок
