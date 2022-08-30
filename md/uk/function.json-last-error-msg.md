Повертає рядок з повідомленням про помилку останнього дзвінка jsonencode() або jsondecode()

-   [« jsonencode](function.json-encode.html)
    
-   [jsonlasterror »](function.json-last-error.html)
    
-   [PHP Manual](index.md)
    
-   [Функции JSON](ref.json.md)
    
-   Повертає рядок з повідомленням про помилку останнього дзвінка jsonencode() або jsondecode()
    

# jsonlasterrormsg

(PHP 5> = 5.5.0, PHP 7, PHP 8)

jsonlasterrormsg — Повертає рядок з повідомленням про помилку останнього дзвінка jsonencode() або jsondecode()

### Опис

```methodsynopsis
json_last_error_msg(): string
```

Повертає текстовий опис останньої помилки, що сталася під час виконання [jsonencode()](function.json-encode.html) або [jsondecode()](function.json-decode.html) без прапора **`JSON_THROW_ON_ERROR`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення про помилку у разі успішного виконання або `"No error"`якщо помилки не сталося.

### Дивіться також

-   [jsonlasterror()](function.json-last-error.html) - Повертає останню помилку