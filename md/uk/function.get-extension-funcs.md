---
navigation:
  - function.get-defined-constants.md: « getdefinedconstants
  - function.get-include-path.md: getincludepath »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getextensionfuncs
---
# getextensionfuncs

(PHP 4, PHP 5, PHP 7, PHP 8)

getextensionfuncs — Повертає масив імен функцій модуля

### Опис

```methodsynopsis
get_extension_funcs(string $extension): array|false
```

Функція повертає імена всіх функцій, визначених у модулі з ім'ям `extension`

### Список параметрів

`extension`

Ім'я модуль.

> **Зауваження**
> 
> Значення цього аргументу має задаватися в *нижньому регістрі*

### Значення, що повертаються

Повертає масив імен функцій або **`false`**, якщо `extension` не є допустимим модулем.

### Приклади

**Приклад #1 Виводить функції XML**

```php
<?php
print_r(get_extension_funcs("xml"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => xml_parser_create
    [1] => xml_parser_create_ns
    [2] => xml_set_object
    [3] => xml_set_element_handler
    [4] => xml_set_character_data_handler
    [5] => xml_set_processing_instruction_handler
    [6] => xml_set_default_handler
    [7] => xml_set_unparsed_entity_decl_handler
    [8] => xml_set_notation_decl_handler
    [9] => xml_set_external_entity_ref_handler
    [10] => xml_set_start_namespace_decl_handler
    [11] => xml_set_end_namespace_decl_handler
    [12] => xml_parse
    [13] => xml_parse_into_struct
    [14] => xml_get_error_code
    [15] => xml_error_string
    [16] => xml_get_current_line_number
    [17] => xml_get_current_column_number
    [18] => xml_get_current_byte_index
    [19] => xml_parser_free
    [20] => xml_parser_set_option
    [21] => xml_parser_get_option
)
```

### Дивіться також

-   [getloadedextensions()](function.get-loaded-extensions.md) - Повертає масив імен усіх скомпілованих та завантажених модулів
-   [ReflectionExtension::getFunctions()](reflectionextension.getfunctions.md) - Отримання функцій модуля
