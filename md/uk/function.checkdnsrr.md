---
navigation:
  - ref.network.md: Мережеві функції
  - function.closelog.md: closelog »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: checkdnsrr
---
# checkdnsrr

(PHP 4, PHP 5, PHP 7, PHP 8)

checkdnsrr — Перевіряє записи DNS, які відповідають переданому імені вузла Інтернету або IP-адресі

### Опис

```methodsynopsis
checkdnsrr(string $hostname, string $type = "MX"): bool
```

Шукає записи DNS типу `type`, відповідні `hostname`

### Список параметрів

`hostname`

Параметр `hostname` може бути IP-адресою у вигляді чотирьох десяткових чисел, розділених крапками, або ім'ям вузла.

`type`

Параметр `type` може бути одним з A, MX, NS, SOA, PTR, CNAME, AAAA, A6, SRV, NAPTR, TXT або ANY.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо були знайдені записи; повертає \*\*`false`\*\*якщо записів не було знайдено або сталася помилка.

### Примітки

> **Зауваження**
> 
> Для сумісності з попередніми версіями PHP під Windows, де не було реалізації цієї функції, використовуйте клас [» PEAR](https://pear.php.net/) [» NetDNS](https://pear.php.net/package/Net_DNS)

### Дивіться також

-   [dnsgetrecord()](function.dns-get-record.md) - Отримання ресурсних записів DNS хоста
-   [getmxrr()](function.getmxrr.md) - Отримує записи MX, що відповідають переданому доменному імені хоста
-   [gethostbyaddr()](function.gethostbyaddr.md) - Отримує доменне ім'я хоста, що відповідає переданій IP-адресі
-   [gethostbyname()](function.gethostbyname.md) - Отримує IPv4-адресу, що відповідає переданому імені хоста
-   [gethostbynamel()](function.gethostbynamel.md) - Отримує список IPv4-адрес, що відповідають переданому доменному імені хоста
-   сторінка керівництва named(8)
