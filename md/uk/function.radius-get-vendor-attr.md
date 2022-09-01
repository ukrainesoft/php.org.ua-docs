---
navigation:
  - function.radius-get-tagged-attr-tag.html: « radiusgettaggedattrtag
  - function.radius-put-addr.html: radiusputaddr »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusgetvendorattr
---
# radiusgetvendorattr

(PECL radius >= 1.1.0)

radiusgetvendorattr — Витягує атрибут, що залежить від постачальника

### Опис

```methodsynopsis
radius_get_vendor_attr(string $data): array
```

Якщо [radiusgetattr()](function.radius-get-attr.md) повернула **`RADIUS_VENDOR_SPECIFIC`** **radiusgetvendorattr()** може бути викликана визначення постачальника.

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

-   [radiusgetattr()](function.radius-get-attr.md) - Витягує атрибут
-   [radiusputvendorattr()](function.radius-put-vendor-attr.md) - Приєднує бінарний атрибут, що залежить від постачальника
