---
navigation:
  - function.dio-truncate.md: « diotruncate
  - book.dir.md: Каталоги »
  - index.md: PHP Manual
  - ref.dio.md: Функції прямого введення/виводу
title: diowrite
---
# diowrite

(PHP 4> = 4.2.0, PHP 5 <5.1.0)

diowrite — Записує байти у файл, опціонально обрізуючи до вказаної довжини

### Опис

```methodsynopsis
dio_write(resource $fd, string $data, int $len = 0): int
```

**diowrite()** записує максимум `len` байт з `data` у файл `fd`

### Список параметрів

`fd`

Файловий дескриптор, отриманий з [dioopen()](function.dio-open.md)

`data`

Дані, що записуються.

`len`

Довжина даних, що записуються в байтах. Якщо не встановлено, то будуть записані всі передані дані.

### Значення, що повертаються

Повертає кількість байт, записаних у `fd`

### Дивіться також

-   [dioread()](function.dio-read.md) - Прочитай байти із файлового дескриптора
