---
navigation:
  - function.radius-create-request.html: « radiuscreaterequest
  - function.radius-cvt-int.html: radiuscvtint »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiuscvtaddr
---
# radiuscvtaddr

(PECL radius >= 1.1.0)

radiuscvtaddr — Перетворює необроблені дані на IP-адресу

### Опис

```methodsynopsis
radius_cvt_addr(string $data): string
```

Перетворює необроблені дані на IP-адресу

### Список параметрів

`data`

Вхідні дані

### Значення, що повертаються

Повертає IP-адресу.

### Приклади

**Приклад #1 Приклад використання **radiuscvtaddr()****

```php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf ("Ошибка при получении атрибута: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];

    switch ($attr) {

    case RADIUS_FRAMED_IP_ADDRESS:
        $ip = radius_cvt_addr($data);
        echo "IP: $ip<br>\n";
        break;

    case RADIUS_FRAMED_IP_NETMASK:
        $mask = radius_cvt_addr($data);
        echo "Маска: $mask<br>\n";
        break;
    }
}
?>
```

### Дивіться також

-   [radiuscvtint()](function.radius-cvt-int.md) - Перетворює необроблені дані на ціле число
-   [radiuscvtstring()](function.radius-cvt-string.md) - Перетворює необроблені дані на рядок
