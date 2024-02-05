---
navigation:
  - eventconfig.setflags.md: '« EventConfig::setFlags'
  - class.eventdnsbase.md: EventDnsBase »
  - index.md: PHP Manual
  - class.eventconfig.md: EventConfig
title: 'EventConfig::setMaxDispatchInterval'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventConfig::setMaxDispatchInterval

(PECL event >= 2.1.0-alpha)

EventConfig::setMaxDispatchInterval — Запобігти інверсії пріоритетів

### Опис

```methodsynopsis
public
   EventConfig::setMaxDispatchInterval(
    int
     $max_interval
   , 
    int
     $max_callbacks
   , 
    int
     $min_priority
   ): void
```

Запобігти інверсії пріоритетів шляхом обмеження кількості оброблюваних низькопріоритетних подій перед черговою перевіркою на наявність більш пріоритетних.

> **Зауваження** :
> 
> Доступно с`libevent 2.1.0-alpha`

### Список параметрів

`max_interval`

Інтервал, після якого Libevent зобов'язаний припинити запускати callback-функції та перевірити наявність нових подій, або щоб не використовувати такий функціонал.

`max_callbacks`

Кількість запущених callback-функцій, після якого Libevent призупинить їх запуск та перевірить, чи є нові події . \*\*`-1`\*\*щоб не використовувати такий функціонал.

`min_priority`

Пріоритет, нижче якого `max_interval`и`max_callbacks` не повинні застосовуватись. Якщо встановлено як , ці обмеження будуть застосовуватися до подій з будь-яким пріоритетом; Якщо встановлено , обмеження будуть застосовуватись до подій пріоритету і вище. І так далі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
