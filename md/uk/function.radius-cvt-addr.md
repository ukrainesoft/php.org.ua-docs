---
navigation:
  - function.radius-create-request.md: « radius\_create\_request
  - function.radius-cvt-int.md: radius\_cvt\_int »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_cvt\_addr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_cvt\_addr

(PECL radius >= 1.1.0)

radius\_cvt\_addr — Перетворює необроблені дані на IP-адресу

### Опис

```methodsynopsis
radius_cvt_addr(string $data): string
```

Перетворює необроблені дані на IP-адресу.

### Список параметрів

`data`

Вхідні дані

### Значення, що повертаються

Повертає IP-адресу.

### Приклади

**Приклад #1 Приклад використання** radius\_cvt\_addr()\*\*\*\*

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

    case RADIUS_FRAMED_IP_ADDRESS:
        $ip = radius_cvt_addr($data);
        echo "IP: $ip<br>\n";
        break;

    case RADIUS_FRAMED_IP_NETMASK:
        $mask = radius_cvt_addr($data);
        echo "Маска: $mask<br>\n";
        break;
    }
}
?>
```

### Дивіться також

-   [radius\_cvt\_int()](function.radius-cvt-int.md) \- Перетворює необроблені дані на ціле число
-   [radius\_cvt\_string()](function.radius-cvt-string.md) \- Перетворює необроблені дані у рядок
