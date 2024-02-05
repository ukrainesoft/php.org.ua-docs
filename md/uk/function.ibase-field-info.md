---
navigation:
  - function.ibase-fetch-row.md: « ibase\_fetch\_row
  - function.ibase-free-event-handler.md: ibase\_free\_event\_handler »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_field\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_field\_info

(PHP 5, PHP 7 < 7.4.0)

ibase\_field\_info — Отримує інформацію про поле

### Опис

```methodsynopsis
ibase_field_info(resource $result, int $field_number): array
```

Повертає масив із інформацією про поле після виконання запиту select.

### Список параметрів

`result`

Ідентифікатор результату InterBase.

`field_number`

Усунення поля.

### Значення, що повертаються

Повертає масив із такими ключами: `name` `alias` `relation` `length`и`type`

### Приклади

**Приклад #1 Приклад використання** ibase\_field\_info()\*\*\*\*

```php
<?php
$rs = ibase_query("SELECT * FROM tablename");
$coln = ibase_num_fields($rs);
for ($i = 0; $i < $coln; $i++) {
    $col_info = ibase_field_info($rs, $i);
    echo "Имя: ". $col_info['name']. "\n";
    echo "Псевдоним: ". $col_info['alias']. "\n";
    echo "Связь: ". $col_info['relation']. "\n";
    echo "Длина: ". $col_info['length']. "\n";
    echo "Тип: ". $col_info['type']. "\n";
}
?>
```

### Дивіться також

-   [ibase\_num\_fields()](function.ibase-num-fields.md) \- Повертає кількість полів у результуючому наборі
