---
navigation:
  - function.stream-context-get-options.html: « streamcontextgetoptions
  - function.stream-context-set-default.html: streamcontextsetdefault »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamcontextgetparams
---
# streamcontextgetparams

(PHP 5> = 5.3.0, PHP 7, PHP 8)

streamcontextgetparams — Отримує параметри з контексту

### Опис

```methodsynopsis
stream_context_get_params(resource $context): array
```

Повертає інформацію про параметри та опції з потоку чи контексту.

### Список параметрів

`context`

Ресурс (resource) потоку чи ресурс (resource) [контекста](context.md)

### Значення, що повертаються

Повертає асоціативний масив, що містить усі опції та параметри контексту.

### Приклади

**Приклад #1 Приклад використання **streamcontextgetparams()****

Приклад простого використання

```php
<?php
$ctx = stream_context_create();
$params = array("notification" => "stream_notification_callback");
stream_context_set_params($ctx, $params);

var_dump(stream_context_get_params($ctx));
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [streamcontextsetoption()](function.stream-context-set-option.md) - Встановлює опцію для потоку/обгортки/контексту
-   [streamcontextsetparams()](function.stream-context-set-params.md) - Встановлює параметри потоку/обгортки/контексту
