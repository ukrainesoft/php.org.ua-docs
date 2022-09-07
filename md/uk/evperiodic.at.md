---
navigation:
  - evperiodic.again.md: '« EvPeriodic::again'
  - evperiodic.construct.md: 'EvPeriodic::construct »'
  - index.md: PHP Manual
  - class.evperiodic.md: EvPeriodic
title: 'EvPeriodic::at'
---
# EvPeriodic::at

(PECL ev >= 0.2.0)

EvPeriodic::at — Повертає абсолютний час, коли спостерігач запуститься наступного разу

### Опис

```methodsynopsis
public
   EvPeriodic::at(): float
```

Якщо спостерігач активний, повертає абсолютний час, коли спостерігач запуститься наступного разу. Це не те ж саме, що аргумент offset для [EvPeriodic::set()](evperiodic.set.md) або [EvPeriodic::construct()](evperiodic.construct.md)він працює навіть в інтервальному режимі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає абсолютний час, коли спостерігач запуститься наступного разу на секунду
