Оновлює файл бази даних RRD

-   [« RRDUpdater::\_\_construct](rrdupdater.construct.html)
    
-   [ScoutAPM »](book.scoutapm.html)
    
-   [PHP Manual](index.html)
    
-   [RRDUpdater](class.rrdupdater.html)
    
-   Оновлює файл бази даних RRD
    

# RRDUpdater::update

(PECL rrd >= 0.9.0)

RRDUpdater::update — Оновлює файл бази даних RRD

### Опис

```methodsynopsis
public RRDUpdater::update(array $values, string $time
     = time()
   ): bool
```

Оновлює файл бази даних RRD, визначений через конструктор [RRDUpdater::\_\_construct()](rrdupdater.construct.html). Файл оновлюється за заданими значеннями.

### Список параметрів

`values`

Дані для поновлення. Масив із ключами, що відповідають іменам джерел даних.

`time`

Значення часу оновлення відповідних даних. За промовчанням використовується поточний час.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

У разі виникнення помилки викидає виняток типу [Exception](class.exception.html)

### Приклади

**Приклад #1 Приклад використання **RRDUpdater::update()****

```php
<?php
$updator = new RRDUpdater("speed.rrd");
//обновляет источник данных "speed" значением "12411"
//для времени заданного временной меткой timestamp "920807700"
$updator->update(array("speed" => "12411"), "920807700");
?>
```