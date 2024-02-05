---
navigation:
  - function.stream-context-get-options.md: « stream\_context\_get\_options
  - function.stream-context-set-default.md: stream\_context\_set\_default »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_context\_get\_params
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_context\_get\_params

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

stream\_context\_get\_params — Отримує параметри з контексту

### Опис

```methodsynopsis
stream_context_get_params(resource $context): array
```

Повертає інформацію про параметри та опції з потоку чи контексту.

### Список параметрів

`context`

Ресурс (resource) потоку чи ресурс (resource) [контексту](context.md)

### Значення, що повертаються

Повертає асоціативний масив, що містить усі опції та параметри контексту.

### Приклади

**Пример #1 Пример использования**stream\_context\_get\_params()\*\*\*\*

Приклад простого використання

```php
<?php
$ctx = stream_context_create();
$params = array("notification" => "stream_notification_callback");
stream_context_set_params($ctx, $params);

var_dump(stream_context_get_params($ctx));
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(2) {
  ["notification"]=>
  string(28) "stream_notification_callback"
  ["options"]=>
  array(0) {
  }
}
```

### Дивіться також

-   [stream\_context\_set\_option()](function.stream-context-set-option.md) \- Встановлює опцію для потоку/обгортки/контексту
-   [stream\_context\_set\_params()](function.stream-context-set-params.md) \- Встановлює параметри потоку/обгортки/контексту
