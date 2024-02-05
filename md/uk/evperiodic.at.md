---
navigation:
  - evperiodic.again.md: '« EvPeriodic::again'
  - evperiodic.construct.md: 'EvPeriodic::\_\_construct »'
  - index.md: PHP Manual
  - class.evperiodic.md: EvPeriodic
title: 'EvPeriodic::at'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvPeriodic::at

(PECL ev >= 0.2.0)

EvPeriodic::at — Повертає абсолютний час, коли спостерігач запуститься наступного разу

### Опис

```methodsynopsis
public
   EvPeriodic::at(): float
```

Якщо спостерігач активний, повертає абсолютний час, коли спостерігач запуститься наступного разу. Це не те ж саме, що аргумент offset для [EvPeriodic::set()](evperiodic.set.md) або [EvPeriodic::\_\_construct()](evperiodic.construct.md)він працює навіть в інтервальному режимі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає абсолютний час, коли спостерігач запуститься наступного разу на секунду
