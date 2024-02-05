---
navigation:
  - function.gethostname.md: « gethostname
  - function.getprotobyname.md: getprotobyname »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: getmxrr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# getmxrr

(PHP 4, PHP 5, PHP 7, PHP 8)

getmxrr — Отримує записи MX, що відповідають переданому домену імені хоста

### Опис

```methodsynopsis
getmxrr(string $hostname, array &$hosts, array &$weights = null): bool
```

Шукає в DNS записи MX, що відповідають `hostname`

### Список параметрів

`hostname`

Ім'я хоста

`hosts`

Список знайдених записів MX, поміщений у масив `hosts`

`weights`

Якщо передано масив `weights`, то він буде заповнений отриманою інформацією про пріоритети.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо були знайдені записи; повертає \*\*`false`\*\*якщо записів не було знайдено або сталася помилка.

### Примітки

> **Зауваження** :
> 
> Ця функція не повинна використовуватись для перевірки адреси. Повертаються тільки поштові сервери, знайдені в DNS, проте, згідно [» RFC 2821](http://www.faqs.org/rfcs/rfc2821), коли у списку немає поштових серверів, необхідно використовувати сам `hostname` як поштовий сервер з пріоритетом

> **Зауваження** :
> 
> Для сумісності з попередніми версіями PHP під Windows, де не було реалізації цієї функції, використовуйте клас [» PEAR](https://pear.php.net/) [» Net\_DNS](https://pear.php.net/package/Net_DNS)

### Дивіться також

-   [checkdnsrr()](function.checkdnsrr.md) \- Перевіряє записи DNS, що відповідають переданому імені вузла Інтернету або IP-адресі
-   [dns\_get\_record()](function.dns-get-record.md) \- Отримання ресурсних записів DNS хоста
-   [gethostbyname()](function.gethostbyname.md) \- Отримує IPv4-адресу, що відповідає переданому імені хоста
-   [gethostbynamel()](function.gethostbynamel.md) \- Отримує список IPv4-адрес, що відповідають переданому доменному імені хоста
-   [gethostbyaddr()](function.gethostbyaddr.md) \- Отримує доменне ім'я хоста, що відповідає переданій IP-адресі
-   сторінка керівництва`named(8)`
