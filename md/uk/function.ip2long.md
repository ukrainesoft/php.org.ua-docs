Конвертує рядок, що містить IPv4-адресу в ціле число

-   [« inetpton](function.inet-pton.html)
    
-   [long2ip »](function.long2ip.md)
    
-   [PHP Manual](index.md)
    
-   [Мережеві функції](ref.network.md)
    
-   Конвертує рядок, що містить IPv4-адресу в ціле число
    

# ip2long

(PHP 4, PHP 5, PHP 7, PHP 8)

ip2long - Конвертує рядок, що містить IPv4-адресу в ціле число

### Опис

```methodsynopsis
ip2long(string $ip): int|false
```

Функція **ip2long()** перетворює IPv4-адресу мережі Інтернет зі стандартного формату (рядок з точками) на ціле число.

Функція **ip2long()** також працюватиме з неповними IP-адресами. Дивіться [» http://publibn.boulder.ibm.com/doclink/enUS/adoclib/libs/commtrf2/inetaddr.htm](http://publibn.boulder.ibm.com/doc_link/en_US/a_doc_lib/libs/commtrf2/inet_addr.htm) для більш детальної інформації.

### Список параметрів

`ip`

Адреса у стандартному форматі.

### Значення, що повертаються

Повертає ціле число або **`false`**, якщо параметр `ip` містить помилку.

### Приклади

**Приклад #1 Приклад використання **ip2long()****

```php
<?php
$ip = gethostbyname('www.example.com');
$out = "Следующие URL эквивалентны:<br />\n";
$out .= 'http://www.example.com/, http://' . $ip . '/, и http://' . sprintf("%u", ip2long($ip)) . "/<br />\n";
echo $out;
?>
```

**Приклад #2 Відображення IP-адрес**

Другий приклад показує, як виводити сконвертовані адреси за допомогою функції [printf()](function.printf.md)

```php
<?php
$ip   = gethostbyname('www.example.com');
$long = ip2long($ip);

if ($long == -1 || $long === FALSE) {
    echo 'Неверный IP-адрес, попробуйте ещё раз';
} else {
    echo $ip   . "\n";            // 192.0.34.166
    echo $long . "\n";            // -1073732954
    printf("%u\n", ip2long($ip)); // 3221234342
}
?>
```

### Примітки

> **Зауваження**
> 
> Зважаючи на те, що тип PHP int є знаковим, і на 32-бітових системах багато IP-адрес будуть представлені у вигляді негативних чисел, необхідно використовувати "%u" у функції [sprintf()](function.sprintf.md) або [printf()](function.printf.md) для отримання IP-адреси у рядковому беззнаковому вигляді.

> **Зауваження**
> 
> Функція **ip2long()** поверне `-1` для IP `255.255.255.255` у 32-бітових системах через цілечисленне переповнення.

### Дивіться також

-   [long2ip()](function.long2ip.md) - Конвертує ціле число в IPv4-адресу
-   [sprintf()](function.sprintf.md) - Повертає відформатований рядок