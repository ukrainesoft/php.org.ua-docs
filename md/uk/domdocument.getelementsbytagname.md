Шукає всі елементи із заданим локальним ім'ям

-   [« DOMDocument::getElementById](domdocument.getelementbyid.html)
    
-   [DOMDocument::getElementsByTagNameNS »](domdocument.getelementsbytagnamens.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Шукає всі елементи із заданим локальним ім'ям
    

# DOMDocument::getElementsByTagName

(PHP 5, PHP 7, PHP 8)

DOMDocument::getElementsByTagName — Шукає всі елементи із заданим локальним ім'ям

### Опис

```methodsynopsis
public DOMDocument::getElementsByTagName(string $qualifiedName): DOMNodeList
```

Ця функція повертає новий об'єкт класу [DOMNodeList](class.domnodelist.html)містить елементи із заданим локальним ім'ям.

### Список параметрів

`qualifiedName`

Локальне ім'я (без простору імен) тега, яким буде проводитися пошук. Спеціальне значення `*` відповідає всім тегам.

### Значення, що повертаються

Новий об'єкт класу [DOMNodeList](class.domnodelist.html)містить всі знайдені елементи.

### Приклади

**Приклад #1 Простий приклад використання**

```php
<?php
$xml = <<< XML
<?xml version="1.0" encoding="utf-8"?>
<books>
 <book>Шаблоны корпоративных приложений</book>
 <book>Приёмы объектно-ориентированного проектирования. Паттерны проектирования</book>
 <book>Чистый код</book>
</books>
XML;

$dom = new DOMDocument;
$dom->loadXML($xml);
$books = $dom->getElementsByTagName('book');
foreach ($books as $book) {
    echo $book->nodeValue, PHP_EOL;
}
?>
```

Результат виконання цього прикладу:

```
Шаблоны корпоративных приложений
Приёмы объектно-ориентированного проектирования. Паттерны проектирования
Чистый код
```

### Дивіться також

-   [DOMDocument::getElementsByTagNameNS()](domdocument.getelementsbytagnamens.html) - Шукає всі елементи із заданим ім'ям у вказаному просторі імен