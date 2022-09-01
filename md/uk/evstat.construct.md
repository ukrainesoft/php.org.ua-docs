---
navigation:
  - evstat.attr.html: '« EvStat::attr'
  - evstat.createstopped.html: 'EvStat::createStopped »'
  - index.html: PHP Manual
  - class.evstat.html: EvStat
title: 'EvStat::construct'
---
# EvStat::construct

(PECL ev >= 0.2.0)

EvStat::construct - Створює об'єкт спостерігача EvStat

### Опис

public **EvStat::construct**  
string `$path`  
float `$interval`  
[callable](language.types.callable.html) `$callback`  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` **`null`**  
int `$priority`

Створює об'єкт спостерігача EvStat та автоматично запускає спостерігача.

### Список параметрів

`path`

Шлях очікування зміни статусу.

`interval`

Підказує, як швидко очікується виявлення змін, та його зазвичай вказується **`0.0`**, щоб дозволити *libev* вибрати потрібне значення.

`callback`

Дивіться [Спостерігачі зворотного виклику](ev.watcher-callbacks.html)

`data`

Дані користувача, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Приклади

**Приклад #1 Дивимося зміни /var/log/messages**

```php
<?php
// Используем 10-секундный интервал обновления.
$w = new EvStat("/var/log/messages", 8, function ($w) {
 echo "/var/log/messages изменён\n";

 $attr = $w->attr();

 if ($attr['nlink']) {
  printf("Размер: %ld\n", $attr['size']);
  printf("Просмотрен: %ld\n", $attr['atime']);
  printf("Изменён: %ld\n", $attr['mtime']);
 } else {
  fprintf(STDERR, "`messages` файл не найден!");
  $w->stop();
 }
});

Ev::run();
?>
```
