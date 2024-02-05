---
navigation:
  - eventdnsbase.clearsearch.md: '« EventDnsBase::clearSearch'
  - eventdnsbase.countnameservers.md: 'EventDnsBase::countNameservers »'
  - index.md: PHP Manual
  - class.eventdnsbase.md: EventDnsBase
title: 'EventDnsBase::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventDnsBase::\_\_construct

(PECL event >= 1.2.6-beta)

EventDnsBase::\_\_construct — Конструктор об'єкта EventDnsBase

### Опис

public**EventDnsBase::\_\_construct** [EventBase](class.eventbase.md) `$base`, int|bool`$initialize`

Створює об'єкт EventDnsBase.

### Список параметрів

`base`

Основа події.

`initialize`

Якщо параметр `initialize`равен\*\*`true`\*\*, він намагається використовувати параметри базової операційної системи за промовчанням для розумного налаштування бази DNS. Якщо він дорівнює **`false`**, база DNS залишається неналаштованою, без серверів імен (nameservers) або набору параметрів. Якщо база DNS залишилася без параметрів, її налаштовують вручну, наприклад методом [EventDnsBase::parseResolvConf()](eventdnsbase.parseresolvconf.md)

Якщо параметр `initialize` передається ціле значення, дозволено відповідність наступним прапорам:

| Flag | Опис |
| --- | --- |
| **`EventDnsBase::DISABLE_WHEN_INACTIVE`** | Не забороняйте вихід з циклу подій модуля будь-якогоvent, коли немає активних DNS-запитів. |
| **`EventDnsBase::INITIALIZE_NAMESERVERS`** | Обработать файл`resolv.conf` |
| **`EventDnsBase::NAMESERVERS_NO_DEFAULT`** | Не додавати сервер імен (nameservers) за замовчуванням, якщо у файлі `resolv.conf`нет записи nameserver. |

### Помилки

Если тип параметра`initialize` відрізняється від перетину типів int|bool, викидається виняток [TypeError](class.typeerror.md)

Если значение параметра`initialize` виявиться неприпустимим, викидається виняток [EventException](class.eventexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL event 3.1.3 | Если тип параметра`initialize` відрізняється від перетину типів int |
| PECL event 3.1.0RC1 | Тип параметра `initialize` змінено з bool на [mixed](language.types.declarations.md#language.types.declarations.mixed). . Дозволено або значення bool (зі збереженням попереднього змісту), або константа з наступного списку: **`EventDnsBase::DISABLE_WHEN_INACTIVE`** **`EventDnsBase::INITIALIZE_NAMESERVERS`**, или\*\*`EventDnsBase::NAMESERVERS_NO_DEFAULT`\*\* |
