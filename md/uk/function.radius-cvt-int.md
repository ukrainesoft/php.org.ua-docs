Перетворює необроблені дані на ціле число

-   [« radius\_cvt\_addr](function.radius-cvt-addr.html)
    
-   [radius\_cvt\_string »](function.radius-cvt-string.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Перетворює необроблені дані на ціле число
    

# radiuscvtint

(PECL radius >= 1.1.0)

radiuscvtint — Перетворює необроблені дані на ціле число

### Опис

```methodsynopsis
radius_cvt_int(string $data): int
```

Перетворює необроблені дані на ціле число

### Список параметрів

`data`

Вхідні дані

### Значення, що повертаються

Повертає ціле число, одержане з даних.

### Приклади

**Приклад #1 Приклад використання **radiuscvtint()****

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

    case RADIUS_FRAMED_MTU:
        $mtu = radius_cvt_int($data);
        echo "Максимальная единица передачи: $mtu<br>\n";
        break;
    }
}
?>
```

### Дивіться також

-   [radius\_cvt\_addr()](function.radius-cvt-addr.html) - Перетворює необроблені дані на IP-адресу
-   [radius\_cvt\_string()](function.radius-cvt-string.html) - Перетворює необроблені дані на рядок