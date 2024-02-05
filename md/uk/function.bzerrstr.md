---
navigation:
  - function.bzerror.md: « bzerror
  - function.bzflush.md: bzflush »
  - index.md: PHP Manual
  - ref.bzip2.md: Функції Bzip2
title: bzerrstr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bzerrstr

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

bzerrstr — Повертає рядок помилки роботи з bzip2

### Опис

```methodsynopsis
bzerrstr(resource $bz): string
```

Повертає рядок з помилкою bzip2, що сталася з переданим покажчиком файлу.

### Список параметрів

`bz`

Вказівник на файл. Має бути коректним і вказувати на файл, успішно відкритий [bzopen()](function.bzopen.md)

### Значення, що повертаються

Повертає рядок, який містить повідомлення про помилку.

### Дивіться також

-   [bzerrno()](function.bzerrno.md) \- Повертає код помилки роботи з bzip2
-   [bzerror()](function.bzerror.md) \- Повертає код та рядок помилки роботи з bzip2 у вигляді масиву
