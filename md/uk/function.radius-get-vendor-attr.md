Витягує атрибут, що залежить від постачальника

-   [« radius\_get\_tagged\_attr\_tag](function.radius-get-tagged-attr-tag.html)
    
-   [radius\_put\_addr »](function.radius-put-addr.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Витягує атрибут, що залежить від постачальника
    

# radiusgetvendorattr

(PECL radius >= 1.1.0)

radiusgetvendorattr — Витягує атрибут, що залежить від постачальника

### Опис

```methodsynopsis
radius_get_vendor_attr(string $data): array
```

Якщо [radius\_get\_attr()](function.radius-get-attr.html) повернула **`RADIUS_VENDOR_SPECIFIC`** **radiusgetvendorattr()** може бути викликана визначення постачальника.

### Список параметрів

`data`

Вхідні дані

### Значення, що повертаються

Повертає асоціативний масив, що містить тип атрибуту, постачальника та дані або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **radiusgetvendorattr()****

```php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf ("Ошибка при получении атрибута: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];
    printf("Получен атрибут:%d %d байт %s\n", $attr, strlen($data), bin2hex($data));
    if ($attr == RADIUS_VENDOR_SPECIFIC) {

        $resv = radius_get_vendor_attr($data);
        if (is_array($resv)) {
            $vendor = $resv['vendor'];
            $attrv = $resv['attr'];
            $datav = $resv['data'];
            printf("Получен атрибут поставщика:%d %d байт %s\n", $attrv, strlen($datav), bin2hex($datav));
        }

    }
}
?>
```

### Дивіться також

-   [radius\_get\_attr()](function.radius-get-attr.html) - Витягує атрибут
-   [radius\_put\_vendor\_attr()](function.radius-put-vendor-attr.html) - Приєднує бінарний атрибут, що залежить від постачальника