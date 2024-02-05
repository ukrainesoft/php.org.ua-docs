---
navigation:
  - function.libxml-set-streams-context.md: « libxml\_set\_streams\_context
  - book.simplexml.md: SimpleXML »
  - index.md: PHP Manual
  - ref.libxml.md: Функції libxml
title: libxml\_use\_internal\_errors
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# libxml\_use\_internal\_errors

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

libxml\_use\_internal\_errors — Вимкнення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві

### Опис

```methodsynopsis
libxml_use_internal_errors(?bool $use_errors = null): bool
```

**libxml\_use\_internal\_errors()** дозволяє вимкнути стандартні помилки libxml і включити користувальницьку обробку помилок.

### Список параметрів

`use_errors`

Включає (**`true`**) користувальницьку обробку помилок або відключає її (**`false`**). Вимкнення також очищає всі поточні помилки libxml.

### Значення, що повертаються

Ця функція повертає попереднє значення параметра `use_errors`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `use_errors` тепер допускає значення null. Раніше значенням за умовчанням було **`false`** |

### Приклади

**Пример #1 Пример использования**libxml\_use\_internal\_errors()\*\*\*\*

Цей приклад демонструє основне використання помилок libxml та значення, яке повертає ця функція.

```php
<?php

// включение обработки ошибок пользователем
var_dump(libxml_use_internal_errors(true));

// загрузка документа
$doc = new DOMDocument;

if (!$doc->load('file.xml')) {
    foreach (libxml_get_errors() as $error) {
        // обработка ошибок здесь
    }

    libxml_clear_errors();
}

?>
```

Результат виконання наведеного прикладу:

```
bool(false)
```

### Дивіться також

-   [libxml\_clear\_errors()](function.libxml-clear-errors.md) \- Очищення буфера помилок libxml
-   [libxml\_get\_errors()](function.libxml-get-errors.md) \- Отримання масиву помилок, що відбулися.
