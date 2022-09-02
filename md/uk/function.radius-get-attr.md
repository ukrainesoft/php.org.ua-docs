---
navigation:
  - function.radius-demangle.md: « radiusdemangle
  - function.radius-get-tagged-attr-data.md: radiusgettaggedattrdata »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusgetattr
---
# radiusgetattr

(PECL radius >= 1.1.0)

radiusgetattr — Витягує атрибут

### Опис

```methodsynopsis
radius_get_attr(resource $radius_handle): mixed
```

Як і запити Radius, кожна відповідь може містити нуль або більше атрибутів. Після того, як відповідь була успішно отримана від [radiussendrequest()](function.radius-send-request.md), його атрибути можуть бути витягнуті один за одним за допомогою **radiusgetattr()**. Щоразу, коли викликається **radiusgetattr()**, функція отримує наступний атрибут із поточної відповіді.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає асоціативний масив, що містить тип атрибуту та дані чи номер помилки <= 0.

### Приклади

**Приклад #1 Приклад використання **radiusgetattr()****

```php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf("Ошибка при получении атрибута: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];
    printf("Получен атрибут: %d %d байт %s\n", $attr, strlen($data), bin2hex($data));
}
?>
```

### Дивіться також

-   [radiusputattr()](function.radius-put-attr.md) - приєднує бінарний атрибут
-   [radiusgetvendorattr()](function.radius-get-vendor-attr.md) - Витягує атрибут, що залежить від постачальника
-   [radiusputvendorattr()](function.radius-put-vendor-attr.md) - Приєднує бінарний атрибут, що залежить від постачальника
-   [radiussendrequest()](function.radius-send-request.md) - Відправляє запит і чекає на відповідь
