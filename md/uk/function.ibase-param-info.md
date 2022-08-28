Повертає інформацію про параметр у підготовленому запиті

-   [« ibase\_num\_params](function.ibase-num-params.html)
    
-   [ibase\_pconnect »](function.ibase-pconnect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Повертає інформацію про параметр у підготовленому запиті
    

# ibaseparaminfo

(PHP 5, PHP 7 < 7.4.0)

ibaseparaminfo — Повертає інформацію про параметр у підготовленому запиті

### Опис

```methodsynopsis
ibase_param_info(resource $query, int $param_number): array
```

Повертає масив з інформацією щодо параметра після підготовки запиту.

### Список параметрів

`query`

Дескриптор підготовленого запиту InterBase

`param_number`

Зміщення параметра.

### Значення, що повертаються

Повертає масив із такими ключами: `name` `alias` `relation` `length` і `type`

### Дивіться також

-   [ibase\_field\_info()](function.ibase-field-info.html) - Отримує інформацію про поле
-   [ibase\_num\_params()](function.ibase-num-params.html) - Повертає кількість параметрів у підготовленому запиті