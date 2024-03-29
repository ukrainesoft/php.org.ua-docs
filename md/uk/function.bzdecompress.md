---
navigation:
  - function.bzcompress.md: « bzcompress
  - function.bzerrno.md: bzerrno »
  - index.md: PHP Manual
  - ref.bzip2.md: Функції Bzip2
title: bzdecompress
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bzdecompress

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

bzdecompress — Розпаковує дані, стиснуті з використанням bzip2

### Опис

```methodsynopsis
bzdecompress(string $data, bool $use_less_memory = false): string|int|false
```

**bzdecompress()** розпаковує переданий рядок, що містить стиснуті bzip2 дані.

### Список параметрів

`data`

Рядок, що розпаковується.

`use_less_memory`

Якщо **`true`**, то буде використаний альтернативний алгоритм розпакування, що використовує менше пам'яті (максимально потрібна пам'ять знаходиться в районі 2300K), але працює приблизно вдвічі повільніше.

Смотрите[» документацію по bzip2](https://www.sourceware.org/bzip2/) для більш детальної інформації про цю можливість.

### Значення, що повертаються

Розпакований рядок або \*\*`false`\*\*или код ошибки в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тип`use_less_memory` змінено з int на bool. Раніше значенням за умовчанням був |

### Приклади

**Приклад #1 Розпакування рядка**

```php
<?php
$start_str = "This is not an honest face?";
$bzstr = bzcompress($start_str);

echo "Compressed String: ";
echo $bzstr;
echo "\n<br />\n";

$str = bzdecompress($bzstr);
echo "Decompressed String: ";
echo $str;
echo "\n<br />\n";
?>
```

### Дивіться також

-   [bzcompress()](function.bzcompress.md) \- Стисне рядок з використанням bzip2
