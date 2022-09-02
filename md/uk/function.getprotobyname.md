---
navigation:
  - function.getmxrr.md: « getmxrr
  - function.getprotobynumber.md: getprotobynumber »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: getprotobyname
---
# getprotobyname

(PHP 4, PHP 5, PHP 7, PHP 8)

getprotobyname — Отримує номер протоколу на ім'я

### Опис

```methodsynopsis
getprotobyname(string $protocol): int|false
```

Функція **getprotobyname()** повертає номер протоколу на ім'я, зазначеному у параметрі `protocol` згідно з /etc/protocols.

### Список параметрів

`protocol`

Ім'я протоколу.

### Значення, що повертаються

Повертає номер протоколу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **getprotobyname()****

```php
<?php
$protocol = 'tcp';
$get_prot = getprotobyname($protocol);
if ($get_prot === FALSE) {
    echo 'Протокол не найден';
} else {
    echo 'Протокол #' . $get_prot;
}
?>
```

### Дивіться також

-   [getprotobynumber()](function.getprotobynumber.md) - Отримує ім'я протоколу за номером
