---
navigation:
  - function.stream-context-get-default.md: « stream\_context\_get\_default
  - function.stream-context-get-params.md: stream\_context\_get\_params »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_context\_get\_options
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_context\_get\_options

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

stream\_context\_get\_options — Отримує опції для потоку/обгортки/контексту

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

**Пример #1 Пример использования**stream\_context\_get\_options()\*\*\*\*

```php
<?php
$params = array("method" => "POST");

stream_context_set_default(array("http" => $params));

var_dump(stream_context_get_options(stream_context_get_default()));

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(1) {
  ["http"]=>
  array(1) {
    ["method"]=>
    string(4) "POST"
  }
}
```
