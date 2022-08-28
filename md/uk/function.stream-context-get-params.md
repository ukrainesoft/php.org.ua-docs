Отримує параметри з контексту

-   [« stream\_context\_get\_options](function.stream-context-get-options.html)
    
-   [stream\_context\_set\_default »](function.stream-context-set-default.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Отримує параметри з контексту
    

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

Ресурс (resource) потоку чи ресурс (resource) [контекста](context.html)

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

-   [stream\_context\_set\_option()](function.stream-context-set-option.html) - Встановлює опцію для потоку/обгортки/контексту
-   [stream\_context\_set\_params()](function.stream-context-set-params.html) - Встановлює параметри потоку/обгортки/контексту