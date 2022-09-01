---
navigation:
  - function.bzdecompress.md: « bzdecompress
  - function.bzerror.md: bzerror »
  - index.md: PHP Manual
  - ref.bzip2.md: Функції Bzip2
title: bzerrno
---
# bzerrno

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

bzerrno — Повертає код помилки роботи з bzip2

### Опис

```methodsynopsis
bzerrno(resource $bz): int
```

Повертає код будь-якої помилки bzip2, що сталася з переданим покажчиком на файл.

### Список параметрів

`bz`

Вказівник на файл. Має бути коректним і вказувати на файл, успішний відкритий [bzopen()](function.bzopen.md)

### Значення, що повертаються

Повертає код помилки як цілого числа.

### Дивіться також

-   [bzerror()](function.bzerror.md) - Повертає код та рядок помилки роботи з bzip2 у вигляді масиву
-   [bzerrstr()](function.bzerrstr.md) - Повертає рядок помилки роботи з bzip2
