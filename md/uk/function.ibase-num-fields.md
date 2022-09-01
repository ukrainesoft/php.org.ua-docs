---
navigation:
  - function.ibase-name-result.html: « ibasenameresult
  - function.ibase-num-params.html: ibasenumparams »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibasenumfields
---
# ibasenumfields

(PHP 5, PHP 7 < 7.4.0)

ibasenumfields — Повертає кількість полів у результуючому наборі

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

**Приклад #1 Приклад використання **ibasenumfields()****

```php
<?php
$rs = ibase_query("SELECT * FROM tablename");
$coln = ibase_num_fields($rs);
for ($i = 0; $i < $coln; $i++) {
    $col_info = ibase_field_info($rs, $i);
    echo "Имя: " . $col_info['name'] . "\n";
    echo "Псевдоним: " . $col_info['alias'] . "\n";
    echo "Связь: " . $col_info['relation'] . "\n";
    echo "Длина: " . $col_info['length'] . "\n";
    echo "Тип: " . $col_info['type'] . "\n";
}
?>
```

### Дивіться також

-   [ibasefieldinfo()](function.ibase-field-info.md) - Отримує інформацію про поле
