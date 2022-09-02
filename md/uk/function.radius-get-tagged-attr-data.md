---
navigation:
  - function.radius-get-attr.md: « radiusgetattr
  - function.radius-get-tagged-attr-tag.md: radiusgettaggedattrtag »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusgettaggedattrdata
---
# radiusgettaggedattrdata

(PECL radius >= 1.3.0)

radiusgettaggedattrdata — Витягує дані із зазначеного атрибуту

### Опис

```methodsynopsis
radius_get_tagged_attr_data(string $data): string|false
```

Якщо з [radiusgetattr()](function.radius-get-attr.md) був повернутий тегований атрибут, **radiusgettaggedattrdata()** поверне тег із атрибуту.

### Список параметрів

`data`

Тегований атрибут, який потрібно розкодувати.

### Значення, що повертаються

Повертає дані з тегованого атрибуту або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **radiusgettaggedattrdata()****

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
-   [radiusgettaggedattrtag()](function.radius-get-tagged-attr-tag.md) - Витягує тег із позначеного атрибуту
