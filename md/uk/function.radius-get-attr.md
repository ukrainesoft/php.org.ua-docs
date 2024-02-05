---
navigation:
  - function.radius-demangle.md: « radius\_demangle
  - function.radius-get-tagged-attr-data.md: radius\_get\_tagged\_attr\_data »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_get\_attr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_get\_attr

(PECL radius >= 1.1.0)

radius\_get\_attr — Витягує атрибут

### Опис

```methodsynopsis
radius_get_attr(resource $radius_handle): mixed
```

Як і запити Radius, кожна відповідь може містити нуль або більше атрибутів. Після того, як відповідь була успішно отримана від [radius\_send\_request()](function.radius-send-request.md), його атрибути можуть бути витягнуті один за одним за допомогою **radius\_get\_attr()**. Щоразу, коли викликається **radius\_get\_attr()**, функція отримує наступний атрибут із поточної відповіді.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає асоціативний масив, що містить тип атрибуту та дані чи номер помилки <= 0.

### Приклади

**Приклад #1 Приклад використання** radius\_get\_attr()\*\*\*\*

```php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf("Ошибка при получении атрибута: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];
    printf("Получен атрибут: %d %d байт %s\n", $attr, strlen($data), bin2hex($data));
}
?>
```

### Дивіться також

-   [radius\_put\_attr()](function.radius-put-attr.md) \- приєднує бінарний атрибут
-   [radius\_get\_vendor\_attr()](function.radius-get-vendor-attr.md) \- Витягує атрибут, що залежить від постачальника
-   [radius\_put\_vendor\_attr()](function.radius-put-vendor-attr.md) \- Приєднує бінарний атрибут, що залежить від постачальника
-   [radius\_send\_request()](function.radius-send-request.md) \- Відправляє запит і чекає на відповідь
