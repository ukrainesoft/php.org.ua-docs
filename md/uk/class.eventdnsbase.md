---
navigation:
  - eventconfig.setmaxdispatchinterval.md: '« EventConfig::setMaxDispatchInterval'
  - eventdnsbase.addnameserverip.md: 'EventDnsBase::addNameserverIp »'
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас EventDnsBase
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

    const
     int
      DISABLE_WHEN_INACTIVE = 32768;

    const
     int
      INITIALIZE_NAMESERVERS = 1;

    const
     int
      NAMESERVERS_NO_DEFAULT = 65536;

    /* Методы */
    
   public
   __construct(
    EventBase
     $base
   , 
    int|bool
     $initialize
   )

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

Вказує читати домен та поля пошуку з файлу `resolv.conf` та опції `ndots` і використовувати їх для визначення доменів (якщо є), в яких буде здійснюватись пошук по короткому імені хоста.

**`EventDnsBase::OPTION_NAMESERVERS`**

Вказує використання серверів імен, вказаних у записі nameservers файлу `resolv.conf`

**`EventDnsBase::OPTION_MISC`**

**`EventDnsBase::OPTION_HOSTSFILE`**

Вказує брати список хостів із файлу `/etc/hosts`при загрузке`resolv.conf`

**`EventDnsBase::OPTIONS_ALL`**

Вказує використовувати все, що можливо, з файлу `resolv.conf`

**`EventDnsBase::DISABLE_WHEN_INACTIVE`**

Не забороняйте вихід з циклу подій модуля будь-якогоvent, коли немає активних DNS-запитів.

**`EventDnsBase::INITIALIZE_NAMESERVERS`**

Обработать файл`resolv.conf`

**`EventDnsBase::NAMESERVERS_NO_DEFAULT`**

Не додавати сервер імен (nameservers) за замовчуванням, якщо у файлі `resolv.conf`нет записи nameserver.

## Зміст

-   [EventDnsBase::addNameserverIp](eventdnsbase.addnameserverip.md)— Додає сервер імен до бази DNS
-   [EventDnsBase::addSearch](eventdnsbase.addsearch.md)— Додає домен до списку пошукових доменів
-   [EventDnsBase::clearSearch](eventdnsbase.clearsearch.md)— Видаляє всі поточні суфікси пошуку
-   [EventDnsBase::\_\_construct](eventdnsbase.construct.md) \- Конструктор об'єкта EventDnsBase
-   [EventDnsBase::countNameservers](eventdnsbase.countnameservers.md)— Отримує кількість налаштованих серверів імен
-   [EventDnsBase::loadHosts](eventdnsbase.loadhosts.md)— Завантажує файл hosts (у тому ж форматі, що й /etc/hosts) із файлу hosts
-   [EventDnsBase::parseResolvConf](eventdnsbase.parseresolvconf.md)— Сканує файл у форматі resolv.conf
-   [EventDnsBase::setOption](eventdnsbase.setoption.md)— Встановлює параметр конфігурації
-   [EventDnsBase::setSearchNdots](eventdnsbase.setsearchndots.md) — Встановлює 'ndots' для пошуку
