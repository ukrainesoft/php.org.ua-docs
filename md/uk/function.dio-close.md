---
navigation:
  - ref.dio.md: « Функції прямого введення/виводу
  - function.dio-fcntl.md: dio\_fcntl »
  - index.md: PHP Manual
  - ref.dio.md: Функції прямого введення/виводу
title: dio\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dio\_close

(PHP 4 >= 4.2.0, PHP 5 < 5.1.0)

dio\_close — Закрити файловий дескриптор

### Опис

```methodsynopsis
dio_close(resource $fd): void
```

Функция**dio\_close()** закриває файловий дескриптор `fd`

### Список параметрів

`fd`

Файловий дескриптор, отриманий з [dio\_open()](function.dio-open.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Закриття файлового дескриптора**

```php
<?php
$fd = dio_open('/dev/ttyS0', O_RDWR);

dio_close($fd);
?>
```

### Дивіться також

-   [dio\_open()](function.dio-open.md) \- Відкриває файл (за потребою створює) на нижчому рівні, ніж потокові функції введення/виведення мови C
