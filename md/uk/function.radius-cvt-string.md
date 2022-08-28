Перетворює необроблені дані на рядок

-   [« radius\_cvt\_int](function.radius-cvt-int.html)
    
-   [radius\_demangle\_mppe\_key »](function.radius-demangle-mppe-key.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Перетворює необроблені дані на рядок
    

# radiuscvtstring

(PECL radius >= 1.1.0)

radiuscvtstring — Перетворює необроблені дані в рядок

### Опис

```methodsynopsis
radius_cvt_string(string $data): string
```

Перетворює необроблені дані на рядок

### Список параметрів

`data`

Вхідні дані

### Значення, що повертаються

Повертає рядок, отриманий із даних.

### Приклади

**Приклад #1 Приклад використання **radiuscvtstring()****

```php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf ("Ошибка при получении атрибута: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];

    switch ($attr) {

    case RADIUS_FILTER_ID:
        $id = radius_cvt_string($data);
        echo "Идентификатор фильтра: $id<br>\n";
        break;
    }
}
?>
```

### Дивіться також

-   [radius\_cvt\_addr()](function.radius-cvt-addr.html) - Перетворює необроблені дані на IP-адресу
-   [radius\_cvt\_int()](function.radius-cvt-int.html) - Перетворює необроблені дані на ціле число