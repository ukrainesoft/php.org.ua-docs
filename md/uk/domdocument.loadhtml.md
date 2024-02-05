---
navigation:
  - domdocument.load.md: '« DOMDocument::load'
  - domdocument.loadhtmlfile.md: 'DOMDocument::loadHTMLFile »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::loadHTML'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::loadHTML

(PHP 5, PHP 7, PHP 8)

DOMDocument::loadHTML — Завантаження HTML з рядка

### Опис

```methodsynopsis
public DOMDocument::loadHTML(string $source, int $options = 0): bool
```

Функція розбирає HTML, що міститься у рядку `source`. На відміну від завантаження XML, HTML не повинен бути правильно побудований для завантаження.

**Увага**

Ця функція аналізує вхідні дані, використовуючи синтаксичний аналізатор HTML 4. У браузері вбудований синтаксичний аналізатор HTML 5, який має інші правила аналізу. Яку структуру DOM буде сформовано — залежить від вхідних даних. Тому цю функцію не можна використовувати для безпечного очищення HTML.

Наприклад, деякі HTML-елементи неявно закриватимуть батьківський елемент. Правила для автоматичного закриття батьківських елементів HTML 4 і HTML 5 різні, тому результуюча структура DOM, яку бачить об'єкт класу [DOMDocument](class.domdocument.md) може відрізнятись від структури DOM, яку бачить веб-браузер, що дає можливість зловмиснику зламати результуючий HTML.

### Список параметрів

`source`

HTML-рядок.

`options`

[Побітове АБО (`OR`) .](language.operators.bitwise.md) [констант опцій libxml](libxml.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо через аргумент `source` передано порожній рядок, буде згенеровано попередження. Це попередження не генерується libxml, тому воно не може бути оброблено функціями обробки помилок libxml.

Незважаючи на те, що некоректний HTML зазвичай успішно завантажується, ця функція може генерувати помилки рівня **`E_WARNING`** при виявленні поганої розмітки. Для обробки цих помилок можна використовувати [функції обробки помилок libxml](function.libxml-use-internal-errors.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер функція має попередній логічний (bool) тип значення, що повертається. |
| 8.0.0 | При статичному виклику функції тепер викидається помилка [Error](class.error.md). . Раніше видавалася помилка рівня **`E_DEPRECATED`** |

### Приклади

**Приклад #1 Створення документа**

```php
<?php
$doc = new DOMDocument();
$doc->loadHTML("<html><body>Test<br></body></html>");
echo $doc->saveHTML();
?>
```

### Дивіться також

-   [DOMDocument::loadHTMLFile()](domdocument.loadhtmlfile.md) \- Завантаження HTML із файлу
-   [DOMDocument::saveHTML()](domdocument.savehtml.md) \- Зберігає документ із внутрішнього подання до рядка, використовуючи форматування HTML
-   [DOMDocument::saveHTMLFile()](domdocument.savehtmlfile.md) \- Зберігає документ із внутрішнього подання до файлу, використовуючи форматування HTML
