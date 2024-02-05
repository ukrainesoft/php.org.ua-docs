---
navigation:
  - function.radius-get-tagged-attr-data.md: « radius\_get\_tagged\_attr\_data
  - function.radius-get-vendor-attr.md: radius\_get\_vendor\_attr »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_get\_tagged\_attr\_tag
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_get\_tagged\_attr\_tag

(PECL radius >= 1.3.0)

radius\_get\_tagged\_attr\_tag — Витягує тег із позначеного атрибуту

### Опис

```methodsynopsis
radius_get_tagged_attr_tag(string $data): int|false
```

Если из[radius\_get\_attr()](function.radius-get-attr.md) був повернутий тегований атрибут, [radius\_get\_tagged\_attr\_data()](function.radius-get-tagged-attr-data.md) поверне тег із атрибуту.

### Список параметрів

`data`

Тегований атрибут, який потрібно розкодувати.

### Значення, що повертаються

Повертає тег із тегованого атрибуту або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**radius\_get\_tagged\_attr\_tag()\*\*\*\*

```php
<?php
while ($resa = radius_get_attr($res)) {
    if (!is_array($resa)) {
        printf ("Ошибка при получении атрибута: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];

    $tag = radius_get_tagged_attr_tag($data);
    $value = radius_get_tagged_attr_data($data);

    printf("Получен тегированный атрибут с тегом %d и значением %s\n", $tag, $value);
}
?>
```

### Дивіться також

-   [radius\_get\_attr()](function.radius-get-attr.md) \- Витягує атрибут
-   [radius\_get\_tagged\_attr\_data()](function.radius-get-tagged-attr-data.md) \- Витягує дані із позначеного атрибуту
