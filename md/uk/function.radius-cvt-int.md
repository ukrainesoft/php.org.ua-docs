---
navigation:
  - function.radius-cvt-addr.md: « radius\_cvt\_addr
  - function.radius-cvt-string.md: radius\_cvt\_string »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_cvt\_int
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_cvt\_int

(PECL radius >= 1.1.0)

radius\_cvt\_int — Перетворює необроблені дані на ціле число

### Опис

```methodsynopsis
radius_cvt_int(string $data): int
```

Перетворює необроблені дані на ціле число.

### Список параметрів

`data`

Вхідні дані

### Значення, що повертаються

Повертає ціле число, одержане з даних.

### Приклади

**Приклад #1 Приклад використання** radius\_cvt\_int()\*\*\*\*

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

    case RADIUS_FRAMED_MTU:
        $mtu = radius_cvt_int($data);
        echo "Максимальная единица передачи: $mtu<br>\n";
        break;
    }
}
?>
```

### Дивіться також

-   [radius\_cvt\_addr()](function.radius-cvt-addr.md) \- Перетворює необроблені дані на IP-адресу
-   [radius\_cvt\_string()](function.radius-cvt-string.md) \- Перетворює необроблені дані у рядок
