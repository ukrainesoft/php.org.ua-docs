---
navigation:
  - domdocument.schemavalidatesource.md: '« DOMDocument::schemaValidateSource'
  - domdocument.xinclude.md: 'DOMDocument::xinclude »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::validate'
---
# DOMDocument::validate

(PHP 5, PHP 7, PHP 8)

DOMDocument::validate — Перевіряє документ на відповідність його DTD

### Опис

```methodsynopsis
public DOMDocument::validate(): bool
```

Перевіряє документ на дійсність, виходячи з його DTD.

Також можна використовувати властивість `validateOnParse` класу [DOMDocument](class.domdocument.md) для перевірки DTD.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо немає DTD, приєднаних до документа, цей метод поверне **`false`**

### Приклади

**Приклад #1 Приклад перевірки DTD**

```php
<?php
$dom = new DOMDocument;
$dom->load('book.xml');
if ($dom->validate()) {
    echo "Документ является действительным!\n";
}
?>
```

Також можна перевіряти XML-файл під час його завантаження:

```php
<?php
$dom = new DOMDocument;
$dom->validateOnParse = true;
$dom->load('book.xml');
?>
```

### Дивіться також

-   [DOMDocument::schemaValidate()](domdocument.schemavalidate.md) - Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.
-   [DOMDocument::schemaValidateSource()](domdocument.schemavalidatesource.md) - Перевіряє дійсність документа, ґрунтуючись на схемі
-   [DOMDocument::relaxNGValidate()](domdocument.relaxngvalidate.md) - Здійснює перевірку документа на правильність побудови за допомогою relaxNG
-   [DOMDocument::relaxNGValidateSource()](domdocument.relaxngvalidatesource.md) - Перевіряє документ за допомогою relaxNG
