---
navigation:
  - function.ob-implicit-flush.md: « obimplicitflush
  - function.ob-start.md: проstart »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: проlisthandlers
---
# проlisthandlers

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

проlisthandlers — Список всіх обробників виводу, що використовуються.

### Опис

```methodsynopsis
ob_list_handlers(): array
```

Список всіх обробників виведення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція поверне масив із використовуваними обробниками виводу (якщо є). Якщо увімкнено [outputbuffering](outcontrol.configuration.md#ini.output-buffering) або використовувалася анонімна функція разом з [проstart()](function.ob-start.md), то **проlisthandlers()** поверне "default output handler".

### Приклади

**Приклад #1 Приклад використання функції **проlisthandlers()****

```php
<?php
//используется output_buffering=On
print_r(ob_list_handlers());
ob_end_flush();

ob_start("ob_gzhandler");
print_r(ob_list_handlers());
ob_end_flush();

// анонимная функция
ob_start(function($string) { return $string; });
print_r(ob_list_handlers());
ob_end_flush();
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => default output handler
)

Array
(
    [0] => ob_gzhandler
)

Array
(
    [0] => Closure::__invoke
)
```

### Дивіться також

-   [проendclean()](function.ob-end-clean.md) - Очистити (стерти) буфер виведення та вимкнути буферизацію виводу
-   [проendflush()](function.ob-end-flush.md) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [проgetflush()](function.ob-get-flush.md) - Скинути буфер виведення, повернути його у вигляді рядка та вимкнути буферизацію виводу
-   [проstart()](function.ob-start.md) - Включення буферизації виводу
