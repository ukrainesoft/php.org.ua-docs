Отримує внутрішні налаштування mbstring

-   [« mberegi](function.mb-eregi.html)
    
-   [мбhttpinput »](function.mb-http-input.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з багатобайтовими рядками](ref.mbstring.html)
    
-   Отримує внутрішні налаштування mbstring
    

# мбgetinfo

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбgetinfo — Отримує внутрішні налаштування mbstring

### Опис

```methodsynopsis
mb_get_info(string $type = "all"): array|string|int|false
```

**мбgetinfo()** повертає внутрішні настройки mbstring.

### Список параметрів

`type`

Якщо `type` не вказано, або вказано як `"all"`, буде повернуто масив (array), що містить елементи `"internal_encoding"` `"http_input"` `"http_output"` `"http_output_conv_mimetypes"` `"mail_charset"` `"mail_header_encoding"` `"mail_body_encoding"` `"illegal_chars"` `"encoding_translation"` `"language"` `"detect_order"` `"substitute_character"` і `"strict_detection"`

Якщо `type` вказано як `"internal_encoding"` `"http_input"` `"http_output"` `"http_output_conv_mimetypes"` `"mail_charset"` `"mail_header_encoding"` `"mail_body_encoding"` `"illegal_chars"` `"encoding_translation"` `"language"` `"detect_order"` `"substitute_character"` або `"strict_detection"`, буде повернуто налаштування вказаного параметра.

### Значення, що повертаються

Масив (array) інформації про параметри, якщо `type` не вказано, інакше значення заданого параметра `type` або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `type` більше не підтримує `"func_overload"` і `"func_overload_list"` |

### Дивіться також

-   [мбregexencoding()](function.mb-regex-encoding.html) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбhttpoutput()](function.mb-http-output.html) - Встановлення/отримання кодування символів виводу HTTP