---
navigation:
  - function.stream-set-blocking.md: « stream\_set\_blocking
  - function.stream-set-read-buffer.md: stream\_set\_read\_buffer »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_set\_chunk\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_set\_chunk\_size

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

stream\_set\_chunk\_size — Встановлює розмір фрагмента потоку даних.

### Опис

```methodsynopsis
stream_set_chunk_size(resource $stream, int $size): int
```

Встановлює розмір фрагмента даних потоку.

### Список параметрів

`stream`

Потік.

`size`

Бажаний розмір фрагмента.

### Значення, що повертаються

Повертає попередній розмір фрагмента у разі успішного виконання.

### Помилки

Викидає виняток [ValueError](class.valueerror.md), если значение параметра`size` менше 1 або більше значення константи **`PHP_INT_MAX`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер викидається виняток[ValueError](class.valueerror.md), если значение параметра`size` менше 1 або більше значення константи **`PHP_INT_MAX`**. . Раніше викликалася помилка рівня **`E_WARNING`** і поверталося логічне значення **`false`** |
