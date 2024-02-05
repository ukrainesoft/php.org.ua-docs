---
navigation:
  - function.radius-config.md: « radius\_config
  - function.radius-cvt-addr.md: radius\_cvt\_addr »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_create\_request
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_create\_request

(PECL radius >= 1.1.0)

radius\_create\_request — Створює обліковий запис або запит автентифікації

### Опис

```methodsynopsis
radius_create_request(resource $radius_handle, int $type): bool
```

Запит Radius складається з коду, що вказує тип запиту, та нуля або більше атрибутів, які надають додаткову інформацію. Щоб розпочати створення нового запиту, викличте **radius\_create\_request()**

> **Зауваження**: Увага: ви повинні викликати цю функцію, перш ніж ви зможете помістити будь-який атрибут!

### Список параметрів

`radius_handle`

`type`

Тип\*\*`RADIUS_ACCESS_REQUEST`** або **`RADIUS_ACCOUNTING_REQUEST`\*\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** radius\_create\_request()\*\*\*\*

```php
<?php
if (!radius_create_request($res, RADIUS_ACCESS_REQUEST)) {
    echo 'RadiusError:' . radius_strerror($res). "\n<br />";
    exit;
}
?>
```

### Дивіться також

-   [radius\_send\_request()](function.radius-send-request.md) \- Відправляє запит і чекає на відповідь
