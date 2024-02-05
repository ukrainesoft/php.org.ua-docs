---
navigation:
  - function.gc-mem-caches.md: « gc\_mem\_caches
  - function.get-cfg-var.md: get\_cfg\_var »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: gc\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gc\_status

(PHP 7 >= 7.3.0, PHP 8)

gc\_status — Повертає інформацію про поточний статус збирача сміття.

### Опис

```methodsynopsis
gc_status(): array
```

Повертає інформацію про поточний статус збирача сміття.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив із такими елементами:

-   `"runs"`
-   `"collected"`
-   `"threshold"`
-   `"roots"`
-   `"running"`
-   `"protected"`
-   `"full"`
-   `"buffer_size"`
-   `"application_time"`
-   `"collector_time"`
-   `"destructor_time"`
-   `"free_time"`

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Теперь функция**gc\_status()** повертає такі додаткові поля: `"running"` `"protected"` `"full"` `"buffer_size"` `"application_time"` `"collector_time"` `"destructor_time"`и`"free_time"` |

### Приклади

**Пример #1 Использование**gc\_status()\*\*\*\*

```php
<?php

// создадим дерево объектов, для которых понадобится собирать мусор
$a = new stdClass();
$a->b = [];
for ($i = 0; $i < 100000; $i++) {
    $b = new stdClass();
    $b->a = $a;
    $a->b[] = $b;
}
unset($a);
unset($b);
gc_collect_cycles();

var_dump(gc_status());
```

Висновок наведеного прикладу буде схожим на:

```
array(4) {
  ["runs"]=>
  int(5)
  ["collected"]=>
  int(100002)
  ["threshold"]=>
  int(50001)
  ["roots"]=>
  int(0)
}
```

Результат виконання наведеного прикладу PHP 8.3 аналогічний:

```
array(12) {
  ["running"]=>
  bool(false)
  ["protected"]=>
  bool(false)
  ["full"]=>
  bool(false)
  ["runs"]=>
  int(5)
  ["collected"]=>
  int(100002)
  ["threshold"]=>
  int(50001)
  ["buffer_size"]=>
  int(131072)
  ["roots"]=>
  int(0)
  ["application_time"]=>
  float(0.031182458)
  ["collector_time"]=>
  float(0.020106291)
  ["destructor_time"]=>
  float(0)
  ["free_time"]=>
  float(0.003707167)
}
```

### Дивіться також

-   [Збір сміття](features.gc.md)
