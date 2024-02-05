---
navigation:
  - function.inet-pton.md: « inet\_pton
  - function.long2ip.md: long2ip »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: ip2long
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ip2long

(PHP 4, PHP 5, PHP 7, PHP 8)

ip2long - Конвертує рядок, що містить IPv4-адресу в ціле число

### Опис

```methodsynopsis
ip2long(string $ip): int|false
```

Функция**ip2long()** перетворює IPv4-адресу мережі Інтернет зі стандартного формату (рядок з точками) на ціле число.

Функция**ip2long()** також працюватиме з неповними IP-адресами. Дивіться [» http://ps-2.kev009.com/wisclibrary/aix52/usr/share/man/info/en\_US/a\_doc\_lib/libs/commtrf2/inet\_addr.htm](http://ps-2.kev009.com/wisclibrary/aix52/usr/share/man/info/en_US/a_doc_lib/libs/commtrf2/inet_addr.htm) для більш детальної інформації.

### Список параметрів

`ip`

Адреса у стандартному форматі.

### Значення, що повертаються

Повертає ціле число або **`false`**, якщо параметр `ip`содержит ошибку.

### Приклади

**Пример #1 Пример использования**ip2long()\*\*\*\*

```php
<?php
$ip = gethostbyname('www.example.com');
$out = "Следующие URL эквивалентны:<br />\n";
$out .= 'http://www.example.com/, http://' . $ip . '/, и http://' . sprintf("%u", ip2long($ip)) . "/<br />\n";
echo $out;
?>
```

**Приклад #2 Відображення IP-адрес**

Другий приклад показує, як виводити сконвертовані адреси за допомогою функції [printf()](function.printf.md) :

```php
<?php
$ip   = gethostbyname('www.example.com');
$long = ip2long($ip);

if ($long == -1 || $long === FALSE) {
    echo 'Неверный IP-адрес, попробуйте ещё раз';
} else {
    echo $ip   . "\n";            // 192.0.34.166
    echo $long . "\n";            // -1073732954
    printf("%u\n", ip2long($ip)); // 3221234342
}
?>
```

### Примітки

> **Зауваження** :
> 
> Зважаючи на те, що тип PHP int є знаковим, і на 32-бітових системах багато IP-адрес будуть представлені у вигляді негативних чисел, необхідно використовувати "%u" у функції [sprintf()](function.sprintf.md) або [printf()](function.printf.md) для отримання IP-адреси у рядковому беззнаковому вигляді.

> **Зауваження** :
> 
> Функция\*\*ip2long()\*\*возвратит`-1`для IP`255.255.255.255` у 32-бітових системах через цілечисленне переповнення.

### Дивіться також

-   [long2ip()](function.long2ip.md) \- Конвертує ціле число в IPv4-адресу
-   [sprintf()](function.sprintf.md) \- Повертає відформатований рядок
