---
navigation:
  - function.radius-get-tagged-attr-tag.md: « radius\_get\_tagged\_attr\_tag
  - function.radius-put-addr.md: radius\_put\_addr »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_get\_vendor\_attr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_get\_vendor\_attr

(PECL radius >= 1.1.0)

radius\_get\_vendor\_attr — Витягує атрибут, що залежить від постачальника

### Опис

```methodsynopsis
radius_get_vendor_attr(string $data): array
```

Якщо [radius\_get\_attr()](function.radius-get-attr.md) повернула **`RADIUS_VENDOR_SPECIFIC`** **radius\_get\_vendor\_attr()** може бути викликана визначення постачальника.

### Список параметрів

`data`

Вхідні дані

### Значення, що повертаються

Повертає асоціативний масив, що містить тип атрибуту, постачальника та дані або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**radius\_get\_vendor\_attr()\*\*\*\*

```php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf ("Ошибка при получении атрибута: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];
    printf("Получен атрибут:%d %d байт %s\n", $attr, strlen($data), bin2hex($data));
    if ($attr == RADIUS_VENDOR_SPECIFIC) {

        $resv = radius_get_vendor_attr($data);
        if (is_array($resv)) {
            $vendor = $resv['vendor'];
            $attrv = $resv['attr'];
            $datav = $resv['data'];
            printf("Получен атрибут поставщика:%d %d байт %s\n", $attrv, strlen($datav), bin2hex($datav));
        }

    }
}
?>
```

### Дивіться також

-   [radius\_get\_attr()](function.radius-get-attr.md) \- Витягує атрибут
-   [radius\_put\_vendor\_attr()](function.radius-put-vendor-attr.md) \- Приєднує бінарний атрибут, що залежить від постачальника
