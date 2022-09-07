---
navigation:
  - function.gzseek.md: « gzseek
  - function.gzuncompress.md: gzuncompress »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: gztell
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

Поточна позиція або **`false`** у разі виникнення помилки.

### Дивіться також

-   [gzopen()](function.gzopen.md) - Відкрити gz-файл
-   [gzseek()](function.gzseek.md) - Перемістити вказівник на позицію в покажчику gz-файлу
-   [gzrewind()](function.gzrewind.md) - Перемістити позицію покажчик gz-файлу на початок
