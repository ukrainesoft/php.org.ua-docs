---
navigation:
  - rrdcreator.addarchive.html: '« RRDCreator::addArchive'
  - rrdcreator.construct.html: 'RRDCreator::construct »'
  - index.html: PHP Manual
  - class.rrdcreator.html: RRDCreator
title: 'RRDCreator::addDataSource'
---
# RRDCreator::addDataSource

(PECL rrd >= 0.9.0)

RRDCreator::addDataSource — Додає визначення джерела даних для бази даних RRD

### Опис

```methodsynopsis
public RRDCreator::addDataSource(string $description): void
```

RRD може приймати введення від декількох джерел даних (ІД), наприклад, з вхідного та вихідного трафіку. Цей метод додає джерело даних щодо опису. Необхідно викликати цей метод для кожного джерела даних.

### Список параметрів

`description`

Визначення джерела даних – ВД. Має той самий формат, що й визначення ІД у команді rrd create. Дивіться сторінку посібника з rrd create для отримання більш детальної інформації.

### Значення, що повертаються

Функція не повертає значення після виконання.
