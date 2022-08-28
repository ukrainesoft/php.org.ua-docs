Отримує опції для потоку/обгортки/контексту

-   [« stream\_context\_get\_default](function.stream-context-get-default.html)
    
-   [stream\_context\_get\_params »](function.stream-context-get-params.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Отримує опції для потоку/обгортки/контексту
    

# streamcontextgetoptions

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

streamcontextgetoptions — Отримує опції для потоку/обгортки/контексту

### Опис

```methodsynopsis
stream_context_get_options(resource $stream_or_context): array
```

Повертає масив опцій у вказаному потоці чи контексті.

### Список параметрів

`stream_or_context`

Потік (stream) або контекст (context), у якого будуть отримані налаштування

### Значення, що повертаються

Повертає асоціативний масив із опціями.

### Приклади

**Приклад #1 Приклад використання **streamcontextgetoptions()****

```php
<?php
$params = array("method" => "POST");

stream_context_set_default(array("http" => $params));

var_dump(stream_context_get_options(stream_context_get_default()));

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  ["http"]=>
  array(1) {
    ["method"]=>
    string(4) "POST"
  }
}
```