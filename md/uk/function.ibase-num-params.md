Повертає кількість параметрів у підготовленому запиті

-   [« ibasenumfields](function.ibase-num-fields.html)
    
-   [ibaseparaminfo »](function.ibase-param-info.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Повертає кількість параметрів у підготовленому запиті
    

# ibasenumparams

(PHP 5, PHP 7 < 7.4.0)

ibasenumparams — Повертає кількість параметрів у підготовленому запиті

### Опис

```methodsynopsis
ibase_num_params(resource $query): int
```

Ця функція повертає кількість параметрів у підготовленому запиті, вказаному `query`. Це кількість сполучних аргументів, які повинні бути присутніми під час виклику [ibaseexecute()](function.ibase-execute.html)

### Список параметрів

`query`

Дескриптор підготовленого запиту

### Значення, що повертаються

Повертає кількість параметрів як цілого числа.

### Дивіться також

-   [ibaseprepare()](function.ibase-prepare.html) - готує запит для подальшого зв'язування псевдозмінних та виконання
-   [ibaseparaminfo()](function.ibase-param-info.html) - Повертає інформацію про параметр у підготовленому запиті