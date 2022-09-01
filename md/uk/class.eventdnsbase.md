---
navigation:
  - eventconfig.setmaxdispatchinterval.md: '« EventConfig::setMaxDispatchInterval'
  - eventdnsbase.addnameserverip.md: 'EventDnsBase::addNameserverIp »'
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас EventDnsBase
---
# Клас EventDnsBase

(PECL event >= 1.2.6-beta)

## Вступ

Представляє структуру бібліотеки DNS Libevent. Використовується для асинхронного дозволу DNS, аналізу конфігураційного файлу resolv.conf і т.д.

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class EventDnsBase
     
     {
    
    /* Константы */
    
     const
     int
      OPTION_SEARCH = 1;

    const
     int
      OPTION_NAMESERVERS = 2;

    const
     int
      OPTION_MISC = 4;

    const
     int
      OPTION_HOSTSFILE = 8;

    const
     int
      OPTIONS_ALL = 15;

    /* Методы */
    
   public
   addNameserverIp(
    string
     $ip
   ): bool
public
   addSearch(
    string
     $domain
   ): void
public
   clearSearch(): void
public
   __construct(
    EventBase
     $base
   , 
    bool
     $initialize
   )
public
   countNameservers(): int
public
   loadHosts(
    string
     $hosts
   ): bool
public
   parseResolvConf(
    int
     $flags
   , 
    string
     $filename
   ): bool
public
   setOption(
    string
     $option
   , 
    string
     $value
   ): bool
public
   setSearchNdots(
    int
     $ndots
   ): bool

   }
```

## Обумовлені константи

**`EventDnsBase::OPTION_SEARCH`**

Вказує читати домен та пошукові поля з файлу `resolv.conf` та опції `ndots` і використовувати їх для визначення доменів (якщо є), в яких здійснюватиметься пошук по короткому імені хоста.

**`EventDnsBase::OPTION_NAMESERVERS`**

Вказує використання сервера імен (nameservers) із файлу `resolv.conf`

**`EventDnsBase::OPTION_MISC`**

**`EventDnsBase::OPTION_HOSTSFILE`**

Вказує брати список хостів із файлу `/etc/hosts` під час завантаження `resolv.conf`

**`EventDnsBase::OPTIONS_ALL`**

Вказує використовувати все, що можливо з файлу `resolv.conf`

## Зміст

-   [EventDnsBase::addNameserverIp](eventdnsbase.addnameserverip.md) — Додає сервер імен до бази DNS
-   [EventDnsBase::addSearch](eventdnsbase.addsearch.md) — Додає домен до списку пошукових доменів
-   [EventDnsBase::clearSearch](eventdnsbase.clearsearch.md) — Видаляє всі поточні суфікси пошуку
-   [EventDnsBase::construct](eventdnsbase.construct.md) - Конструктор об'єкта EventDnsBase
-   [EventDnsBase::countNameservers](eventdnsbase.countnameservers.md) — Отримує кількість налаштованих серверів імен
-   [EventDnsBase::loadHosts](eventdnsbase.loadhosts.md) — Завантажує файл hosts (у тому форматі, що і /etc/hosts) з файлу hosts
-   [EventDnsBase::parseResolvConf](eventdnsbase.parseresolvconf.md) — Сканує файл у форматі resolv.conf
-   [EventDnsBase::setOption](eventdnsbase.setoption.md) — Встановлює параметр конфігурації
-   [EventDnsBase::setSearchNdots](eventdnsbase.setsearchndots.md) — Встановлює 'ndots' для пошуку
