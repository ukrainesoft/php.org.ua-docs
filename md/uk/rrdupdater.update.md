---
navigation:
  - rrdupdater.construct.md: '« RRDUpdater::construct'
  - book.scoutapm.md: ScoutAPM »
  - index.md: PHP Manual
  - class.rrdupdater.md: RRDUpdater
title: 'RRDUpdater::update'
---
# RRDUpdater::update

(PECL rrd >= 0.9.0)

RRDUpdater::update — Оновлює файл бази даних RRD

### Опис

```methodsynopsis
public RRDUpdater::update(array $values, string $time
     = time()
   ): bool
```

Оновлює файл бази даних RRD, визначений через конструктор [RRDUpdater::construct()](rrdupdater.construct.md). Файл оновлюється за заданими значеннями.

### Список параметрів

`values`

Дані для поновлення. Масив із ключами, що відповідають іменам джерел даних.

`time`

Значення часу оновлення відповідних даних. За промовчанням використовується поточний час.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

У разі виникнення помилки викидає виняток типу [Exception](class.exception.md)

### Приклади

**Приклад #1 Приклад використання **RRDUpdater::update()****

```php
<?php
$updator = new RRDUpdater("speed.rrd");
//обновляет источник данных "speed" значением "12411"
//для времени заданного временной меткой timestamp "920807700"
$updator->update(array("speed" => "12411"), "920807700");
?>
```
