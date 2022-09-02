---
navigation:
  - function.dio-open.md: « dioopen
  - function.dio-seek.md: dioseek »
  - index.md: PHP Manual
  - ref.dio.md: Функції прямого введення/виводу
title: dioread
---
# dioread

(PHP 4> = 4.2.0, PHP 5 <5.1.0)

dioread — Прочитай байти із файлового дескриптора

### Опис

```methodsynopsis
dio_read(resource $fd, int $len = 1024): string
```

Функція **dioread()** читає та повертає `len` байт із дескриптора `fd`

### Список параметрів

`fd`

Файловий дескриптор, отриманий з [dioopen()](function.dio-open.md)

`len`

Кількість байт для читання. Якщо не поставлено, то **dioread()** прочитає блок 1 кілобайт.

### Значення, що повертаються

Байти читатимуться з `fd`

### Дивіться також

-   [diowrite()](function.dio-write.md) - Записує байти у файл, опціонально обрізаючи до вказаної довжини
