---
navigation:
  - function.radius-cvt-addr.md: « radiuscvtaddr
  - function.radius-cvt-string.md: radiuscvtstring »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiuscvtint
---
# radiuscvtint

(PECL radius >= 1.1.0)

radiuscvtint — Перетворює необроблені дані на ціле число

### Опис

```methodsynopsis
radius_cvt_int(string $data): int
```

Перетворює необроблені дані на ціле число

### Список параметрів

`data`

Вхідні дані

### Значення, що повертаються

Повертає ціле число, одержане з даних.

### Приклади

**Приклад #1 Приклад використання **radiuscvtint()****

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

-   [radiuscvtaddr()](function.radius-cvt-addr.md) - Перетворює необроблені дані на IP-адресу
-   [radiuscvtstring()](function.radius-cvt-string.md) - Перетворює необроблені дані на рядок
