---
navigation:
  - function.radius-config.html: « radiusconfig
  - function.radius-cvt-addr.html: radiuscvtaddr »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiuscreaterequest
---
# radiuscreaterequest

(PECL radius >= 1.1.0)

radiuscreaterequest — Створює обліковий запис або запит автентифікації

### Опис

```methodsynopsis
radius_create_request(resource $radius_handle, int $type): bool
```

Запит Radius складається з коду, що вказує тип запиту, та нуля або більше атрибутів, які надають додаткову інформацію. Щоб розпочати створення нового запиту, викличте **radiuscreaterequest()**

> **Зауваження**: Увага: ви повинні викликати цю функцію, перш ніж ви зможете помістити будь-який атрибут!

### Список параметрів

`radius_handle`

`type`

Тип **`RADIUS_ACCESS_REQUEST`** або **`RADIUS_ACCOUNTING_REQUEST`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **radiuscreaterequest()****

```php
<?php
if (!radius_create_request($res, RADIUS_ACCESS_REQUEST)) {
    echo 'RadiusError:' . radius_strerror($res). "\n<br />";
    exit;
}
?>
```

### Дивіться також

-   [radiussendrequest()](function.radius-send-request.html) - Відправляє запит і чекає на відповідь
