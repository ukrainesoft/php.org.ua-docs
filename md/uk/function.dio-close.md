---
navigation:
  - ref.dio.md: « Функції прямого введення/виводу
  - function.dio-fcntl.md: diofcntl »
  - index.md: PHP Manual
  - ref.dio.md: Функції прямого введення/виводу
title: dioclose
---
# dioclose

(PHP 4> = 4.2.0, PHP 5 <5.1.0)

dioclose — Закрити файловий дескриптор

### Опис

```methodsynopsis
dio_close(resource $fd): void
```

Функція **dioclose()** закриває файловий дескриптор `fd`

### Список параметрів

`fd`

Файловий дескриптор, отриманий з [dioopen()](function.dio-open.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Закриття файлового дескриптора**

```php
<?php
$fd = dio_open('/dev/ttyS0', O_RDWR);

dio_close($fd);
?>
```

### Дивіться також

-   [dioopen()](function.dio-open.md) - Відкриває файл (за потребою створює) на нижчому рівні, ніж потокові функції введення/виведення мови C
