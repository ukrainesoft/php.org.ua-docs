---
navigation:
  - domdocument.load.html: '« DOMDocument::load'
  - domdocument.loadhtmlfile.html: 'DOMDocument::loadHTMLFile »'
  - index.html: PHP Manual
  - class.domdocument.html: DOMDocument
title: 'DOMDocument::loadHTML'
---
# DOMDocument::loadHTML

(PHP 5, PHP 7, PHP 8)

DOMDocument::loadHTML — Завантаження HTML з рядка

### Опис

```methodsynopsis
public DOMDocument::loadHTML(string $source, int $options = 0): DOMDocument|bool
```

Функція розбирає HTML, що міститься у рядку `source`. На відміну від завантаження XML HTML не повинен бути правильно побудованим (well-formed) документом. Ця функція також може бути викликана статично для завантаження та створення об'єкта класу [DOMDocument](class.domdocument.html). Статичний виклик може використовуватися у випадках, коли немає потреби встановлювати значення параметрів об'єкта [DOMDocument](class.domdocument.md) до завантаження документа.

### Список параметрів

`source`

HTML-рядок.

`options`

Починаючи з версії Libxml 2.6.0 можна також використовувати параметр `options` для вказівки [додаткових параметрів Libxml](libxml.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. У разі статичного виклику повертає об'єкт класу [DOMDocument](class.domdocument.md) або **`false`** у разі виникнення помилки.

### Помилки

Якщо через аргумент `source` передано порожній рядок, буде згенеровано попередження. Це попередження не генерується libxml, тому воно не може бути оброблено функціями обробки помилок libxml.

До PHP 8.0.0 метод *може* викликатись статично, але викличе помилку **`E_DEPRECATED`**. Починаючи з PHP 8.0.0, виклик цього методу статично викидає виняток [Error](class.error.md)

Незважаючи на те, що некоректний HTML зазвичай успішно завантажується, ця функція може генерувати помилки рівня **`E_WARNING`** при виявленні поганої розмітки. Для обробки даних помилок можна скористатися [функциями обработки ошибок libxml](function.libxml-use-internal-errors.md)

### Приклади

**Приклад #1 Створення документа**

```php
<?php
$doc = new DOMDocument();
$doc->loadHTML("<html><body>Test<br></body></html>");
echo $doc->saveHTML();
?>
```

### Дивіться також

-   [DOMDocument::loadHTMLFile()](domdocument.loadhtmlfile.md) - Завантаження HTML із файлу
-   [DOMDocument::saveHTML()](domdocument.savehtml.md) - Зберігає документ із внутрішнього подання до рядка, використовуючи форматування HTML
-   [DOMDocument::saveHTMLFile()](domdocument.savehtmlfile.md) - Зберігає документ із внутрішнього подання до файлу, використовуючи форматування HTML
