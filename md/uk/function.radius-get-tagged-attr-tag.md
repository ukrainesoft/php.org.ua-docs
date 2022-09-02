---
navigation:
  - function.radius-get-tagged-attr-data.md: « radiusgettaggedattrdata
  - function.radius-get-vendor-attr.md: radiusgetvendorattr »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusgettaggedattrtag
---
# radiusgettaggedattrtag

(PECL radius >= 1.3.0)

radiusgettaggedattrtag — Витягує тег із позначеного атрибуту

### Опис

```methodsynopsis
radius_get_tagged_attr_tag(string $data): int|false
```

Якщо з [radiusgetattr()](function.radius-get-attr.md) був повернутий тегований атрибут, [radiusgettaggedattrdata()](function.radius-get-tagged-attr-data.md) поверне тег із атрибуту.

### Список параметрів

`data`

Тегований атрибут, який потрібно розкодувати.

### Значення, що повертаються

Повертає тег із тегованого атрибуту або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **radiusgettaggedattrtag()****

```php
<?php
while ($resa = radius_get_attr($res)) {
    if (!is_array($resa)) {
        printf ("Ошибка при получении атрибута: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];

    $tag = radius_get_tagged_attr_tag($data);
    $value = radius_get_tagged_attr_data($data);

    printf("Получен тегированный атрибут с тегом %d и значением %s\n", $tag, $value);
}
?>
```

### Дивіться також

-   [radiusgetattr()](function.radius-get-attr.md) - Витягує атрибут
-   [radiusgettaggedattrdata()](function.radius-get-tagged-attr-data.md) - Витягує дані із позначеного атрибуту
