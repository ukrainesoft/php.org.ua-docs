---
navigation:
  - function.radius-cvt-int.md: « radius\_cvt\_int
  - function.radius-demangle-mppe-key.md: radius\_demangle\_mppe\_key »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_cvt\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_cvt\_string

(PECL radius >= 1.1.0)

radius\_cvt\_string — Перетворює необроблені дані в рядок

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

**Приклад #1 Приклад использования функции**radius\_cvt\_string()\*\*\*\*

```php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf ("Ошибка при получении атрибута: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];

    switch ($attr) {

    case RADIUS_FILTER_ID:
        $id = radius_cvt_string($data);
        echo "Идентификатор фильтра: $id<br>\n";
        break;
    }
}
?>
```

### Дивіться також

-   [radius\_cvt\_addr()](function.radius-cvt-addr.md) \- Перетворює необроблені дані на IP-адресу
-   [radius\_cvt\_int()](function.radius-cvt-int.md) \- Перетворює необроблені дані на ціле число
