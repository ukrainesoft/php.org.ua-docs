---
navigation:
  - class.rrdcreator.md: « RRDCreator
  - rrdcreator.adddatasource.md: 'RRDCreator::addDataSource »'
  - index.md: PHP Manual
  - class.rrdcreator.md: RRDCreator
title: 'RRDCreator::addArchive'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RRDCreator::addArchive

(PECL rrd >= 0.9.0)

RRDCreator::addArchive — Додає RRA - архів значень даних для кожного джерела даних

### Опис

```methodsynopsis
public RRDCreator::addArchive(string $description): void
```

Додає визначення RRA щодо опису архіву. Архів складається з низки значень даних чи статистики кожному за певних джерел даних (ІД). Джерела даних визначаються методом [RRDCreator::addDataSource()](rrdcreator.adddatasource.md). Необхідно викликати цей метод кожному за запитаного архіву.

### Список параметрів

`description`

Визначення архіву – RRA. Має той самий формат, як і визначення RRA у команді rrd create. Дивіться сторінку посібника з rrd create для отримання більш детальної інформації.

### Значення, що повертаються

Функція не повертає значення після виконання.
