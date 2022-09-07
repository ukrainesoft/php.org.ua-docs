---
navigation:
  - function.libxml-set-streams-context.md: « libxmlsetstreamscontext
  - book.simplexml.md: SimpleXML »
  - index.md: PHP Manual
  - ref.libxml.md: Функції libxml
title: libxmluseinternalerrors
---
# libxmluseinternalerrors

(PHP 5> = 5.1.0, PHP 7, PHP 8)

libxmluseinternalerrors — Вимкнення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві

### Опис

```methodsynopsis
libxml_use_internal_errors(?bool $use_errors = null): bool
```

**libxmluseinternalerrors()** дозволяє вимкнути стандартні помилки libxml і включити користувальницьку обробку помилок.

### Список параметрів

`use_errors`

Включає (**`true`**) користувальницьку обробку помилок або відключає її (**`false`**). Вимкнення також очищає всі поточні помилки libxml.

### Значення, що повертаються

Ця функція повертає попереднє значення параметра `use_errors`

### список змін

| Версия | Описание |
| --- | --- |
|  | `use_errors` тепер допускає значення null. Раніше значенням за умовчанням було **`false`** |

### Приклади

**Приклад #1 Приклад використання **libxmluseinternalerrors()****

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

Результат виконання цього прикладу:

```
bool(false)
```

### Дивіться також

-   [libxmlclearerrors()](function.libxml-clear-errors.md) - Очищення буфера помилок libxml
-   [libxmlgeterrors()](function.libxml-get-errors.md) - Отримання масиву помилок, що відбулися.
