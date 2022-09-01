---
navigation:
  - evperiodic.again.html: '« EvPeriodic::again'
  - evperiodic.construct.html: 'EvPeriodic::construct »'
  - index.html: PHP Manual
  - class.evperiodic.html: EvPeriodic
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

Якщо спостерігач активний, повертає абсолютний час, коли спостерігач запуститься наступного разу. Це не те ж саме, що аргумент offset для [EvPeriodic::set()](evperiodic.set.html) або [EvPeriodic::construct()](evperiodic.construct.html)він працює навіть в інтервальному режимі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає абсолютний час, коли спостерігач запуститься наступного разу на секунду
