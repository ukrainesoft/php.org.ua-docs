Завантаження HTML із файлу

-   [« DOMDocument::loadHTML](domdocument.loadhtml.html)
    
-   [DOMDocument::loadXML »](domdocument.loadxml.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Завантаження HTML із файлу
    

# DOMDocument::loadHTMLFile

(PHP 5, PHP 7, PHP 8)

DOMDocument::loadHTMLFile — Завантаження HTML із файлу

### Опис

```methodsynopsis
public DOMDocument::loadHTMLFile(string $filename, int $options = 0): DOMDocument|bool
```

Функція розбирає HTML-документ із файлу `filename`. На відміну від завантаження XML HTML не повинен бути правильно побудованим (well-formed).

### Список параметрів

`filename`

Шлях до HTML-файлу.

`options`

Починаючи з версії Libxml 2.6.0 можна також використовувати параметр `options` для вказівки [дополнительных параметров Libxml](libxml.constants.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо викликана статично, повертає об'єкт класу [DOMDocument](class.domdocument.html) або **`false`** у разі виникнення помилки.

### Помилки

Якщо через аргумент `filename` передано порожній рядок або файл нічого не містить, буде згенеровано попередження. Це попередження не генерується libxml, тому воно не може бути оброблено [функциями обработки ошибок libxml](function.libxml-use-internal-errors.html)

До PHP 8.0.0 метод *може* викликатись статично, але викличе помилку **`E_DEPRECATED`**. Починаючи з PHP 8.0.0, виклик цього методу статично викидає виняток [Error](class.error.html)

Незважаючи на те, що некоректний HTML зазвичай успішно завантажується, ця функція може генерувати помилки рівня **`E_WARNING`** при виявленні поганої розмітки. Для обробки даних помилок можна скористатися [функциями обработки ошибок libxml](function.libxml-use-internal-errors.html)

### Приклади

**Приклад #1 Створення документа**

```php
<?php
$doc = new DOMDocument();
$doc->loadHTMLFile("filename.html");
echo $doc->saveHTML();
?>
```

### Дивіться також

-   [DOMDocument::loadHTML()](domdocument.loadhtml.html) - Завантаження HTML з рядка
-   [DOMDocument::saveHTML()](domdocument.savehtml.html) - Зберігає документ із внутрішнього подання до рядка, використовуючи форматування HTML
-   [DOMDocument::saveHTMLFile()](domdocument.savehtmlfile.html) - Зберігає документ із внутрішнього подання до файлу, використовуючи форматування HTML