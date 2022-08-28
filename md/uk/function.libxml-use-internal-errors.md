Відключення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві

-   [« libxml\_set\_streams\_context](function.libxml-set-streams-context.html)
    
-   [SimpleXML »](book.simplexml.html)
    
-   [PHP Manual](index.html)
    
-   [Функции libxml](ref.libxml.html)
    
-   Відключення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві
    

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

// включение обработки ошибок пользователем
var_dump(libxml_use_internal_errors(true));

// загрузка документа
$doc = new DOMDocument;

if (!$doc->load('file.xml')) {
    foreach (libxml_get_errors() as $error) {
        // обработка ошибок здесь
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

-   [libxml\_clear\_errors()](function.libxml-clear-errors.html) - Очищення буфера помилок libxml
-   [libxml\_get\_errors()](function.libxml-get-errors.html) - Отримання масиву помилок, що відбулися.