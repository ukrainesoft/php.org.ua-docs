---
navigation:
  - function.getmxrr.md: « getmxrr
  - function.getprotobynumber.md: getprotobynumber »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: getprotobyname
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# getprotobyname

(PHP 4, PHP 5, PHP 7, PHP 8)

getprotobyname — Отримує номер протоколу на ім'я

### Опис

```methodsynopsis
getprotobyname(string $protocol): int|false
```

Функция**getprotobyname()** повертає номер протоколу на ім'я, зазначеному у параметрі `protocol`согласно /etc/protocols.

### Список параметрів

`protocol`

Ім'я протоколу.

### Значення, що повертаються

Повертає номер протоколу або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**getprotobyname()\*\*\*\*

```php
<?php
$protocol = 'tcp';
$get_prot = getprotobyname($protocol);
if ($get_prot === FALSE) {
    echo 'Протокол не найден';
} else {
    echo 'Протокол #' . $get_prot;
}
?>
```

### Дивіться також

-   [getprotobynumber()](function.getprotobynumber.md) \- Отримує ім'я протоколу за номером
