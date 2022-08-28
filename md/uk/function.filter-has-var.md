Перевіряє існування змінної вказаного типу

-   [« Функции фильтрации данных](ref.filter.html)
    
-   [filter\_id »](function.filter-id.html)
    
-   [PHP Manual](index.html)
    
-   [Функции фильтрации данных](ref.filter.html)
    
-   Перевіряє існування змінної вказаного типу
    

# filterhasvar

(PHP 5> = 5.2.0, PHP 7, PHP 8)

filterhasvar — Перевіряє існування змінної вказаного типу

### Опис

```methodsynopsis
filter_has_var(int $input_type, string $var_name): bool
```

### Список параметрів

`input_type`

Один з **`INPUT_GET`** **`INPUT_POST`** **`INPUT_COOKIE`** **`INPUT_SERVER`** **`INPUT_ENV`**

`var_name`

Ім'я змінної, що перевіряється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.