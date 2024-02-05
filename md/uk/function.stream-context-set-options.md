---
navigation:
  - function.stream-context-set-option.md: « stream\_context\_set\_option
  - function.stream-context-set-params.md: stream\_context\_set\_params »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_context\_set\_options
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_context\_set\_options

(PHP 8 >= 8.3.0)

stream\_context\_set\_options — Встановлює опції заданого контексту

### Опис

```methodsynopsis
stream_context_set_options(resource $context, array $options): bool
```

Встановлює опції у заданому контексті.

### Список параметрів

`context`

Ресурс потоку чи контексту для встановлення опцій.

`options`

Опция для установки ресурсу`context`

> **Зауваження** :
> 
> Параметр`options` має бути асоціативним масивом (array) асоціативних масивів у форматі `$array['wrapper']['option'] = $value`
> 
> Опції потоку перераховані у розділі «[Контекстні опції та параметри](context.md)».

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования функции**stream\_context\_set\_options()\*\*\*\*

```php
<?php

$context = stream_context_create();

$options = [
    'http' => [
        'protocol_version' => 1.1,
        'user_agent' => 'PHPT Agent',
    ],
];

stream_context_set_options($context, $options);
var_dump(stream_context_get_options($context));
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  ["http"]=>
  array(2) {
    ["protocol_version"]=>
    float(1.1)
    ["user_agent"]=>
    string(10) "PHPT Agent"
  }
}
```

### Дивіться також

-   [stream\_context\_set\_option()](function.stream-context-set-option.md) \- Встановлює опцію для потоку/обгортки/контексту
