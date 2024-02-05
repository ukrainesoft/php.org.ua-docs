---
navigation:
  - function.mqseries-set.md: « mqseries\_set
  - book.network.md: Мережа "
  - index.md: PHP Manual
  - ref.mqseries.md: Функції mqseries
title: mqseries\_strerror
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mqseries\_strerror

(PECL mqseries >= 0.10.0)

mqseries\_strerror — Отримати повідомлення про помилку, яке відповідає її коду (MQRC)

### Опис

```methodsynopsis
mqseries_strerror(int $reason): string
```

Функция**mqseries\_strerror()** повертає повідомлення про помилку відповідно до її коду.

### Список параметрів

`reason`

Код помилки.

### Значення, що повертаються

рядок із описом помилки.

### Приклади

**Приклад #1 Приклад використання** mqseries\_strerror()\*\*\*\*

```php
<?php
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("open CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
?>
```

Результат виконання наведеного прикладу:

```
Connx CompCode:2 Reason:2059 Text:Queue manager not available for connection.
```
