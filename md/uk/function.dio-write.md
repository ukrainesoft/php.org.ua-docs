---
navigation:
  - function.dio-truncate.md: « dio\_truncate
  - book.dir.md: Каталоги »
  - index.md: PHP Manual
  - ref.dio.md: Функції прямого введення/виводу
title: dio\_write
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dio\_write

(PHP 4 >= 4.2.0, PHP 5 < 5.1.0)

dio\_write — Записує байти у файл, опціонально обрізуючи до вказаної довжини

### Опис

```methodsynopsis
dio_write(resource $fd, string $data, int $len = 0): int
```

**dio\_write()** записує максимум `len`байт из`data` у файл `fd`

### Список параметрів

`fd`

Файловий дескриптор, отриманий з [dio\_open()](function.dio-open.md)

`data`

Дані, що записуються.

`len`

Довжина даних, що записуються в байтах. Якщо не встановлено, то будуть записані всі передані дані.

### Значення, що повертаються

Повертає кількість байт, записаних у `fd`

### Дивіться також

-   [dio\_read()](function.dio-read.md) \- Прочитай байти із файлового дескриптора
