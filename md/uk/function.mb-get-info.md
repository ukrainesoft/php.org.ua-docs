---
navigation:
  - function.mb-eregi.md: « mb\_eregi
  - function.mb-http-input.md: mb\_http\_input »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_get\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_get\_info

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_get\_info — Отримує внутрішні налаштування mbstring

### Опис

```methodsynopsis
mb_get_info(string $type = "all"): array|string|int|false
```

Функция**mb\_get\_info()** повертає внутрішні параметри налаштувань mbstring.

### Список параметрів

`type`

Якщо параметр `type` не заданий або заданий як `"all"`, буде повернено масив (array), що містить елементи `"internal_encoding"` `"http_input"` `"http_output"` `"http_output_conv_mimetypes"` `"mail_charset"` `"mail_header_encoding"` `"mail_body_encoding"` `"illegal_chars"` `"encoding_translation"` `"language"` `"detect_order"` `"substitute_character"`и`"strict_detection"`

Якщо параметр `type`задан как`"internal_encoding"` `"http_input"` `"http_output"` `"http_output_conv_mimetypes"` `"mail_charset"` `"mail_header_encoding"` `"mail_body_encoding"` `"illegal_chars"` `"encoding_translation"` `"language"` `"detect_order"` `"substitute_character"`или`"strict_detection"`, буде повернуто налаштування вказаного параметра.

### Значення, що повертаються

Повертає масив інформації про параметри, якщо параметр `type` не визначено, інакше значення заданого параметра `type`или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`type` більше не підтримує значення `"func_overload"`и`"func_overload_list"` |

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.md) \- Встановлює/отримує кодування символів для однобайтового регулярного виразу
-   [mb\_http\_output()](function.mb-http-output.md) \- Встановлює/отримує кодування символів виводу HTTP
