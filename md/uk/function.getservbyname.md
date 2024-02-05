---
navigation:
  - function.getprotobynumber.md: « getprotobynumber
  - function.getservbyport.md: getservbyport »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: getservbyname
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# getservbyname

(PHP 4, PHP 5, PHP 7, PHP 8)

getservbyname — Отримує номер порту, пов'язаного з інтернет-службою та протоколом

### Опис

```methodsynopsis
getservbyname(string $service, string $protocol): int|false
```

Функция**getservbyname()** повертає порт, який відповідає параметру `service`для заданного протокола в параметре`protocol`согласно /etc/services.

### Список параметрів

`service`

Ім'я служби Інтернету у вигляді рядка.

`protocol`

Параметр`protocol` може дорівнювати `"tcp"`или`"udp"` (У нижньому регістрі).

### Значення, що повертаються

Повертає номер порту, або **`false`**, якщо `service`или`protocol` не знайдено.

### Приклади

**Приклад #1 Приклад використання** getservbyname()\*\*\*\*

```php
<?php
$services = array('http', 'ftp', 'ssh', 'telnet', 'imap',
'smtp', 'nicname', 'gopher', 'finger', 'pop3', 'www');

foreach ($services as $service) {
    $port = getservbyname($service, 'tcp');
    echo $service . ": " . $port . "<br />\n";
}
?>
```

### Дивіться також

-   [getservbyport()](function.getservbyport.md) \- Отримує інтернет-службу, що відповідає заданому порту та протоколу
-   Смотрите[» http://www.iana.org/assignments/port-numbers](http://www.iana.org/assignments/port-numbers)щоб отримати повний список номерів портів.
