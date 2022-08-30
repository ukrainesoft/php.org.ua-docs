Створює екземпляр SNMP, що представляє сесію віддаленого агента SNMP

-   [« SNMP::close](snmp.close.html)
    
-   [SNMP::get »](snmp.get.html)
    
-   [PHP Manual](index.html)
    
-   [SNMP](class.snmp.html)
    
-   Створює екземпляр SNMP, що представляє сесію віддаленого агента SNMP
    

# SNMP::construct

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SNMP::construct - Створює екземпляр SNMP, що представляє сесію віддаленого агента SNMP

### Опис

public **SNMP::construct**  
int `$version`  
string `$hostname`  
string `$community`  
int `$timeout`  
int `$retries`

Опис функції

### Список параметрів

`version`

SNMP protocol version: **`SNMP::VERSION_1`** **`SNMP::VERSION_2C`** **`SNMP::VERSION_3`**

`hostname`

Агент SNMP . `hostname` може мати суфікс з необов'язковим портом агента SNMP після двокрапки. Адреси IPv6 повинні бути укладені у квадратні дужки, якщо використовуються з портом. Якщо для `hostname` використовується повне доменне ім'я, воно буде опрацьовано бібліотекою php-snmp, а не механізмом Net-SNMP. Використання IPv6-адрес при вказівці повного доменного імені може бути примусово поміщено у квадратні дужки. Ось кілька прикладів:

< td>IPv6 з стандартним портом

<table class="doctable table"><tbody class="tbody"><tr><td>IPv4 з стандартним портом</td><td>127.0.0.1</td></tr><tr><td>::1 or [::1]</td></tr><tr><td>IPv4 з конкретним портом</td><td>127.0. 0.1:1161</td></tr><tr><td>IPv6 з конкретним портом</td><td>[::1]:1161</td></tr><tr><td>FQDN з стандартним портом</td><td>host.domain</td></tr><tr><td>FQDN з конкретним портом</td><td>host.domain:1161</td></tr><tr><td>FQDN з стандартним портом, примусове використання IPv6-адреси</td><td>[host.domain]</td></tr><tr><td>FQDN з конкретним портом, примусове використання IPv6-адреси</td><td>[host.domain]:1161</td></tr></tbody></table>

`community`

Призначення `community` залежить від версії SNMP:

`timeout`

Кількість мікросекунд до першого часу очікування.

`retries`

Кількість повторних спроб у разі перевищення часу очікування.

### Помилки

**SNMP::construct()** викидає виняток, коли кількість або типи параметрів неправильні або вказана невідома версія протоколу SNMP.

### Приклади

**Приклад #1 Отримання sysLocation**

```php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $sysdescr = $session->get("sysDescr.0");
  echo "$sysdescr\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
STRING: Test server
```

### Дивіться також

-   [SNMP::close()](snmp.close.html) - Закриває сесію SNMP

<table class="doctable table"><tbody class="tbody"><tr><td>SNMP::VERSION_1</td><td><abbr title="Simple Network Management Protocol">SNMP</abbr> community</td></tr><tr><td>SNMP::VERSION_2C</td><td><abbr title="Simple Network Management Protocol">SNMP</abbr> community</td></tr><tr><td>SNMP::VERSION_3</td><td><abbr title="Simple Network Management Protocol">SNMP</abbr>v3 securityName</td></tr></tbody></table>