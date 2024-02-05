---
navigation:
  - datetime.modify.md: '« DateTime::modify'
  - datetime.setdate.md: 'DateTime::setDate »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::\_\_set\_state'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTime::\_\_set\_state

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DateTime::\_\_set\_state — Обработчик\_\_set\_state

### Опис

```methodsynopsis
public static DateTime::__set_state(array $array): DateTime
```

Обработчик[\_\_set\_state()](language.oop5.magic.md#object.set-state)

Подобен методу[DateTimeImmutable::\_\_set\_state()](datetimeimmutable.set-state.md), крім роботи з об'єктом [DateTime](class.datetime.md)

### Список параметрів

`array`

Масив для ініціалізації.

### Значення, що повертаються

Повертає новий екземпляр класу DateTime.
