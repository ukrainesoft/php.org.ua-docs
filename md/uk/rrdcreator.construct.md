---
navigation:
  - rrdcreator.adddatasource.md: '« RRDCreator::addDataSource'
  - rrdcreator.save.md: 'RRDCreator::save »'
  - index.md: PHP Manual
  - class.rrdcreator.md: RRDCreator
title: 'RRDCreator::construct'
---
# RRDCreator::construct

(PECL rrd >= 0.9.0)

RRDCreator::construct — Створює новий екземпляр [RRDCreator](class.rrdcreator.md)

### Опис

public **RRDCreator::construct**(string `$path`, string `$startTime` =?, int `$step`

Створює новий екземпляр [RRDCreator](class.rrdcreator.md)

### Список параметрів

`path`

Шлях до створеного файлу бази даних RRD.

`startTime`

Час для першого значення бази даних RRD. Параметр підтримує всі формати, які підтримуються викликом rrd create.

int`step`

Базовий інтервал у секундах, з яким дані завантажуватимуться в базу даних RRD.
