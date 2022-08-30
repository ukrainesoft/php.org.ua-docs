Отримує записи MX, що відповідають переданому доменному імені хоста

-   [« gethostname](function.gethostname.html)
    
-   [getprotobyname »](function.getprotobyname.html)
    
-   [PHP Manual](index.html)
    
-   [Мережеві функції](ref.network.html)
    
-   Отримує записи MX, що відповідають переданому доменному імені хоста
    

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

> **Зауваження**
> 
> Ця функція не повинна використовуватись для перевірки адреси. Повертаються тільки поштові сервери, знайдені в DNS, проте, згідно [» RFC 2821](http://www.faqs.org/rfcs/rfc2821), коли у списку немає поштових серверів, необхідно використовувати сам `hostname` як поштовий сервер з пріоритетом `0`

> **Зауваження**
> 
> Для сумісності з попередніми версіями PHP під Windows, де не було реалізації цієї функції, використовуйте клас [» PEAR](https://pear.php.net/) [» NetDNS](https://pear.php.net/package/Net_DNS)

### Дивіться також

-   [checkdnsrr()](function.checkdnsrr.html) - Перевіряє записи DNS, що відповідають переданому імені вузла Інтернету або IP-адресі
-   [dnsgetrecord()](function.dns-get-record.html) - Отримання ресурсних записів DNS хоста
-   [gethostbyname()](function.gethostbyname.html) - Отримує IPv4-адресу, що відповідає переданому імені хоста
-   [gethostbynamel()](function.gethostbynamel.html) - Отримує список IPv4-адрес, що відповідають переданому доменному імені хоста
-   [gethostbyaddr()](function.gethostbyaddr.html) - Отримує доменне ім'я хоста, що відповідає переданій IP-адресі
-   сторінка керівництва `named(8)`