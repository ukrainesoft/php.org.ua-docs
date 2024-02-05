---
navigation:
  - function.json-encode.md: « json\_encode
  - function.json-last-error.md: json\_last\_error »
  - index.md: PHP Manual
  - ref.json.md: Функції JSON
title: json\_last\_error\_msg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# json\_last\_error\_msg

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

json\_last\_error\_msg — Повертає рядок із повідомленням про помилку останнього дзвінка json\_encode() або json\_decode()

### Опис

```methodsynopsis
json_last_error_msg(): string
```

Повертає текстовий опис останньої помилки, що сталася під час виконання [json\_encode()](function.json-encode.md) або [json\_decode()](function.json-decode.md)без флага\*\*`JSON_THROW_ON_ERROR`\*\*

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення про помилку у разі успішного виконання або `"No error"`якщо помилки не сталося.

### Дивіться також

-   [json\_last\_error()](function.json-last-error.md) \- Повертає останню помилку
