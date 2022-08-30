Надає ім'я набору результатів

-   [« ibasemodifyuser](function.ibase-modify-user.html)
    
-   [ibasenumfields »](function.ibase-num-fields.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Надає ім'я набору результатів
    

# ibasenameresult

(PHP 5, PHP 7 < 7.4.0)

ibasenameresult — Надає ім'я набору результатів.

### Опис

```methodsynopsis
ibase_name_result(resource $result, string $name): bool
```

Функція надає ім'я набору результатів. Ім'я може бути використане пізніше у запитах UPDATE | DELETE ... WHERE CURRENT OF `name`

### Список параметрів

`result`

Набір результатів InterBase.

`name`

Ім'я призначення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ibasenameresult()****

```php
<?php
$result = ibase_query("SELECT field1,field2 FROM table FOR UPDATE");
ibase_name_result($result, "my_cursor");

$updateqry = ibase_prepare("UPDATE table SET field2 = ? WHERE CURRENT OF my_cursor");

for ($i = 0; ibase_fetch_row($result); ++$i) {
    ibase_execute($updateqry, $i);
}
?>
```

### Дивіться також

-   [ibaseprepare()](function.ibase-prepare.html) - готує запит для подальшого зв'язування псевдозмінних та виконання
-   [ibaseexecute()](function.ibase-execute.html) - Виконує попередньо підготовлений запит