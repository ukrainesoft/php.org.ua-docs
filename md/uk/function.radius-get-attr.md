Витягує атрибут

-   [« radius\_demangle](function.radius-demangle.html)
    
-   [radius\_get\_tagged\_attr\_data »](function.radius-get-tagged-attr-data.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Витягує атрибут
    

# radiusgetattr

(PECL radius >= 1.1.0)

radiusgetattr — Витягує атрибут

### Опис

```methodsynopsis
radius_get_attr(resource $radius_handle): mixed
```

Як і запити Radius, кожна відповідь може містити нуль або більше атрибутів. Після того, як відповідь була успішно отримана від [radius\_send\_request()](function.radius-send-request.html), його атрибути можуть бути витягнуті один за одним за допомогою **radiusgetattr()**. Щоразу, коли викликається **radiusgetattr()**, функція отримує наступний атрибут із поточної відповіді.

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

-   [radius\_put\_attr()](function.radius-put-attr.html) - приєднує бінарний атрибут
-   [radius\_get\_vendor\_attr()](function.radius-get-vendor-attr.html) - Витягує атрибут, що залежить від постачальника
-   [radius\_put\_vendor\_attr()](function.radius-put-vendor-attr.html) - Приєднує бінарний атрибут, що залежить від постачальника
-   [radius\_send\_request()](function.radius-send-request.html) - Відправляє запит і чекає на відповідь