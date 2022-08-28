Додає сервер імен до бази DNS

-   [« EventDnsBase](class.eventdnsbase.html)
    
-   [EventDnsBase::addSearch »](eventdnsbase.addsearch.html)
    
-   [PHP Manual](index.html)
    
-   [EventDnsBase](class.eventdnsbase.html)
    
-   Додає сервер імен до бази DNS
    

# EventDnsBase::addNameserverIp

(PECL event >= 1.2.6-beta)

EventDnsBase::addNameserverIp — Додає сервер імен до бази DNS

### Опис

```methodsynopsis
public
   EventDnsBase::addNameserverIp(
    string
     $ip
   ): bool
```

Додає сервер імен до бази evdnsbase.

### Список параметрів

`ip`

Рядок сервера імен у вигляді адреси IPv4, IPv6, IPv4 з портом (`IPv4:Port`) або IPv6 адреси з портом (`[IPv6]:Port`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.