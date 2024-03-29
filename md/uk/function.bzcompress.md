---
navigation:
  - function.bzclose.md: « bzclose
  - function.bzdecompress.md: bzdecompress »
  - index.md: PHP Manual
  - ref.bzip2.md: Функції Bzip2
title: bzcompress
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bzcompress

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

bzcompress — Стискає рядок за допомогою bzip2

### Опис

```methodsynopsis
bzcompress(string $data, int $block_size = 4, int $work_factor = 0): string|int
```

**bzcompress()** стискає переданий рядок і повертає його у вигляді закодованих даних bzip2.

### Список параметрів

`data`

Стиснутий рядок.

`block_size`

Визначає розмір блоку, що використовується при стисканні, повинен бути числом в діапазоні від 1 до 9, де 9 дасть найкраще, але більш ресурсомісткий стиск.

`work_factor`

Контролює поведінку фази компресії у гіршому випадку, коли вхідні дані часто повторюються. Параметр може набувати значення між 0 і 250, де 0 означає спеціальний випадок.

Результат, що генерується, не залежить від параметра `work_factor` і є одним і тим самим.

### Значення, що повертаються

Стиснутий рядок або код помилки у разі невдалого завершення роботи.

### Приклади

**Приклад #1 Стиснення даних**

```php
<?php
$str = "sample data";
$bzstr = bzcompress($str, 9);
echo $bzstr;
?>
```

### Дивіться також

-   [bzdecompress()](function.bzdecompress.md) \- Розпаковує дані, стиснуті з використанням bzip2
