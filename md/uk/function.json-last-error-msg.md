Повертає рядок з повідомленням про помилку останнього дзвінка jsonencode() або jsondecode()

-   [« json\_encode](function.json-encode.html)
    
-   [json\_last\_error »](function.json-last-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции JSON](ref.json.html)
    
-   Повертає рядок з повідомленням про помилку останнього дзвінка jsonencode() або jsondecode()
    

# jsonlasterrormsg

(PHP 5> = 5.5.0, PHP 7, PHP 8)

jsonlasterrormsg — Повертає рядок з повідомленням про помилку останнього дзвінка jsonencode() або jsondecode()

### Опис

```methodsynopsis
json_last_error_msg(): string
```

Повертає текстовий опис останньої помилки, що сталася під час виконання [json\_encode()](function.json-encode.html) або [json\_decode()](function.json-decode.html) без прапора **`JSON_THROW_ON_ERROR`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає повідомлення про помилку у разі успішного виконання або `"No error"`якщо помилки не сталося.

### Дивіться також

-   [json\_last\_error()](function.json-last-error.html) - Повертає останню помилку