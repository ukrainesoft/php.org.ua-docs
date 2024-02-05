---
navigation:
  - function.dio-stat.md: « dio\_stat
  - function.dio-truncate.md: dio\_truncate »
  - index.md: PHP Manual
  - ref.dio.md: Функції прямого введення/виводу
title: dio\_tcsetattr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dio\_tcsetattr

(PHP 4 >= 4.3.0, PHP 5 < 5.1.0)

dio\_tcsetattr — Встановлює атрибути терміналу та швидкість передачі даних для послідовного порту

### Опис

```methodsynopsis
dio_tcsetattr(resource $fd, array $options): bool
```

**dio\_tcsetattr()** встановлює атрибути терміналу та швидкість передачі даних послідовного порту для дескриптора `fd`

### Список параметрів

`fd`

Файловий дескриптор, отриманий з [dio\_open()](function.dio-open.md)

`options`

Доступні опції:

-   'baud' - швидкість передачі для послідовного порту: 38400, 19200, 9600, 4800, 2400, 1800, 1200, 600, 300, 200, 150, 134, 110, 75 або 50.
    
-   'bits' - біти даних: 8, 7, 6 або 5. За замовчуванням 8.
    
-   'stop' – стоп біти: 1 або 2. За замовчуванням 1.
    
-   'parity' - парність: 0, 1 або 2. За замовчуванням 0.
    

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Встановлення швидкості передачі для послідовного порту**

```php
<?php

$fd = dio_open('/dev/ttyS0', O_RDWR | O_NOCTTY | O_NONBLOCK);

dio_fcntl($fd, F_SETFL, O_SYNC);

dio_tcsetattr($fd, array(
  'baud' => 9600,
  'bits' => 8,
  'stop'  => 1,
  'parity' => 0
));

while (1) {

  $data = dio_read($fd, 256);

  if ($data) {
      echo $data;
  }
}

?>
```

### Примітки

> **Зауваження**: Для Windows-платформ ця функція не реалізована.
