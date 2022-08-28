Отримує інформацію про поле

-   [« ibase\_fetch\_row](function.ibase-fetch-row.html)
    
-   [ibase\_free\_event\_handler »](function.ibase-free-event-handler.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Отримує інформацію про поле
    

# ibasefieldinfo

(PHP 5, PHP 7 < 7.4.0)

ibasefieldinfo — Отримує інформацію про поле

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

Повертає масив із такими ключами: `name` `alias` `relation` `length` і `type`

### Приклади

**Приклад #1 Приклад використання **ibasefieldinfo()****

```php
<?php
$rs = ibase_query("SELECT * FROM tablename");
$coln = ibase_num_fields($rs);
for ($i = 0; $i < $coln; $i++) {
    $col_info = ibase_field_info($rs, $i);
    echo "Имя: ". $col_info['name']. "\n";
    echo "Псевдоним: ". $col_info['alias']. "\n";
    echo "Связь: ". $col_info['relation']. "\n";
    echo "Длина: ". $col_info['length']. "\n";
    echo "Тип: ". $col_info['type']. "\n";
}
?>
```

### Дивіться також

-   [ibase\_num\_fields()](function.ibase-num-fields.html) - Повертає кількість полів у результуючому наборі