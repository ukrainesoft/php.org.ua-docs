Отримати повідомлення про помилку, що відповідає її коду (MQRC)

-   [« mqseriesset](function.mqseries-set.html)
    
-   [Сеть »](book.network.html)
    
-   [PHP Manual](index.html)
    
-   [Функции mqseries](ref.mqseries.html)
    
-   Отримати повідомлення про помилку, що відповідає її коду (MQRC)
    

# mqseriesstrerror

(PECL mqseries >= 0.10.0)

mqseriesstrerror — Отримати повідомлення про помилку, яке відповідає її коду (MQRC)

### Опис

```methodsynopsis
mqseries_strerror(int $reason): string
```

Функція **mqseriesstrerror()** повертає повідомлення про помилку відповідно до її коду.

### Список параметрів

`reason`

Код помилки.

### Значення, що повертаються

рядок із описом помилки.

### Приклади

**Приклад #1 Приклад використання **mqseriesstrerror()****

```php
<?php
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("open CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
?>
```

Результат виконання цього прикладу:

```
Connx CompCode:2 Reason:2059 Text:Queue manager not available for connection.
```