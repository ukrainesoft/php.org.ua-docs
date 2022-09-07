---
navigation:
  - datetime.modify.md: '« DateTime::modify'
  - datetime.setdate.md: 'DateTime::setDate »'
  - index.md: PHP Manual
  - class.datetime.md: DateTime
title: 'DateTime::setstate'
---
# DateTime::setstate

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DateTime::setstate - Оброблювач setstate

### Опис

```methodsynopsis
public static DateTime::__set_state(array $array): DateTime
```

Обробник [setstate()](language.oop5.magic.md#object.set-state)

Подібний до методу [DateTimeImmutable::setstate()](datetimeimmutable.set-state.md), крім роботи з об'єктом [DateTime](class.datetime.md)

### Список параметрів

`array`

Масив для ініціалізації.

### Значення, що повертаються

Повертає новий екземпляр класу DateTime.
