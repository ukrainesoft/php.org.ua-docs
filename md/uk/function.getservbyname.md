Отримує номер порту, пов'язаного з інтернет-службою та протоколом

-   [« getprotobynumber](function.getprotobynumber.html)
    
-   [getservbyport »](function.getservbyport.html)
    
-   [PHP Manual](index.html)
    
-   [Мережеві функції](ref.network.html)
    
-   Отримує номер порту, пов'язаного з інтернет-службою та протоколом
    

# getservbyname

(PHP 4, PHP 5, PHP 7, PHP 8)

getservbyname — Отримує номер порту, пов'язаного з інтернет-службою та протоколом

### Опис

```methodsynopsis
getservbyname(string $service, string $protocol): int|false
```

Функція **getservbyname()** повертає порт, який відповідає параметру `service` для заданого протоколу у параметрі `protocol` згідно з /etc/services.

### Список параметрів

`service`

Ім'я служби Інтернету у вигляді рядка.

`protocol`

Параметр `protocol` може дорівнювати `"tcp"` або `"udp"` (У нижньому регістрі).

### Значення, що повертаються

Повертає номер порту, або **`false`**, якщо `service` або `protocol` не знайдено.

### Приклади

**Приклад #1 Приклад використання **getservbyname()****

```php
<?php
$services = array('http', 'ftp', 'ssh', 'telnet', 'imap',
'smtp', 'nicname', 'gopher', 'finger', 'pop3', 'www');

foreach ($services as $service) {
    $port = getservbyname($service, 'tcp');
    echo $service . ": " . $port . "<br />\n";
}
?>
```

### Дивіться також

-   [getservbyport()](function.getservbyport.html) - Отримує інтернет-службу, що відповідає заданому порту та протоколу
-   Дивіться [» http://www.iana.org/assignments/port-numbers](http://www.iana.org/assignments/port-numbers) щоб отримати повний список номерів портів.