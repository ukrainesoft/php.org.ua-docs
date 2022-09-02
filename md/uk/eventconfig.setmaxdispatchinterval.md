---
navigation:
  - eventconfig.setflags.md: '« EventConfig::setFlags'
  - class.eventdnsbase.md: EventDnsBase »
  - index.md: PHP Manual
  - class.eventconfig.md: EventConfig
title: 'EventConfig::setMaxDispatchInterval'
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

> **Зауваження**
> 
> Доступно з `libevent 2.1.0-alpha`

### Список параметрів

`max_interval`

Інтервал, після якого Libevent зобов'язаний припинити запускати callback-функції та перевірити наявність нових подій, або \*\*`0`\*\*щоб не використовувати такий функціонал.

`max_callbacks`

Кількість запущених callback-функцій, після якого Libevent призупинить їх запуск та перевірить, чи є нові події . \*\*`-1`\*\*щоб не використовувати такий функціонал.

`min_priority`

Пріоритет, нижче якого `max_interval` і `max_callbacks` не повинні застосовуватись. Якщо встановлено як **`0`**, ці обмеження будуть застосовуватися до подій з будь-яким пріоритетом; Якщо встановлено **`1`** , обмеження будуть застосовуватись до подій пріоритету **`1`** і вище. І так далі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
