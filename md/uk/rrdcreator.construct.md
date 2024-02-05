---
navigation:
  - rrdcreator.adddatasource.md: '« RRDCreator::addDataSource'
  - rrdcreator.save.md: 'RRDCreator::save »'
  - index.md: PHP Manual
  - class.rrdcreator.md: RRDCreator
title: 'RRDCreator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RRDCreator::\_\_construct

(PECL rrd >= 0.9.0)

RRDCreator::\_\_construct — Створює новий екземпляр [RRDCreator](class.rrdcreator.md)

### Опис

public **RRDCreator::\_\_construct**(string`$path`, string`$startTime`\= ?, int`$step`

Створює новий екземпляр [RRDCreator](class.rrdcreator.md)

### Список параметрів

`path`

Шлях до створеного файлу бази даних RRD.

`startTime`

Час для першого значення бази даних RRD. Параметр підтримує всі формати, які підтримуються викликом rrd create.

int`step`

Базовий інтервал у секундах, з яким дані завантажуватимуться в базу даних RRD.
