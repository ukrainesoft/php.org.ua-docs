---
navigation:
  - function.ibase-name-result.md: « ibase\_name\_result
  - function.ibase-num-params.md: ibase\_num\_params »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_num\_fields
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_num\_fields

(PHP 5, PHP 7 < 7.4.0)

ibase\_num\_fields — Повертає кількість полів у результуючому наборі

### Опис

```methodsynopsis
ibase_num_fields(resource $result_id): int
```

Повертає кількість полів у результуючому наборі.

### Список параметрів

`result_id`

Ідентифікатор результату InterBase.

### Значення, що повертаються

Повертає кількість полів як цілого числа.

### Приклади

**Пример #1 Пример использования**ibase\_num\_fields()\*\*\*\*

```php
<?php
$rs = ibase_query("SELECT * FROM tablename");
$coln = ibase_num_fields($rs);
for ($i = 0; $i < $coln; $i++) {
    $col_info = ibase_field_info($rs, $i);
    echo "Имя: " . $col_info['name'] . "\n";
    echo "Псевдоним: " . $col_info['alias'] . "\n";
    echo "Связь: " . $col_info['relation'] . "\n";
    echo "Длина: " . $col_info['length'] . "\n";
    echo "Тип: " . $col_info['type'] . "\n";
}
?>
```

### Дивіться також

-   [ibase\_field\_info()](function.ibase-field-info.md) \- Отримує інформацію про поле
