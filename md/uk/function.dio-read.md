---
navigation:
  - function.dio-open.md: « dio\_open
  - function.dio-seek.md: dio\_seek »
  - index.md: PHP Manual
  - ref.dio.md: Функції прямого введення/виводу
title: dio\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dio\_read

(PHP 4 >= 4.2.0, PHP 5 < 5.1.0)

dio\_read — Прочитай байти із файлового дескриптора

### Опис

```methodsynopsis
dio_read(resource $fd, int $len = 1024): string
```

Функция**dio\_read()** читає та повертає `len`байт из дескриптора`fd`

### Список параметрів

`fd`

Файловий дескриптор, отриманий з [dio\_open()](function.dio-open.md)

`len`

Кількість байт для читання. Якщо не поставлено, то **dio\_read()** прочитає блок 1 кілобайт.

### Значення, що повертаються

Байти читатимуться з `fd`

### Дивіться також

-   [dio\_write()](function.dio-write.md) \- Записує байти у файл, опціонально обрізаючи до вказаної довжини
