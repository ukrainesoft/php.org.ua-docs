Завантажує файл hosts (у тому форматі, що і /etc/hosts) з файлу hosts

-   [« EventDnsBase::countNameservers](eventdnsbase.countnameservers.html)
    
-   [EventDnsBase::parseResolvConf »](eventdnsbase.parseresolvconf.html)
    
-   [PHP Manual](index.html)
    
-   [EventDnsBase](class.eventdnsbase.html)
    
-   Завантажує файл hosts (у тому форматі, що і /etc/hosts) з файлу hosts
    

# EventDnsBase::loadHosts

(PECL event >= 1.2.6-beta)

EventDnsBase::loadHosts — Завантажує файл hosts (у тому ж форматі, що і /etc/hosts) з файлу hosts

### Опис

```methodsynopsis
public
   EventDnsBase::loadHosts(
    string
     $hosts
   ): bool
```

Завантажує файл hosts (у тому ж форматі, що й `/etc/hosts`) з файлу hosts.

### Список параметрів

`hosts`

Шлях до файлу хостів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.