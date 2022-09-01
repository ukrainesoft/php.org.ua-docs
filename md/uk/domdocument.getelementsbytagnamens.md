---
navigation:
  - domdocument.getelementsbytagname.html: '« DOMDocument::getElementsByTagName'
  - domdocument.importnode.html: 'DOMDocument::importNode »'
  - index.html: PHP Manual
  - class.domdocument.html: DOMDocument
title: 'DOMDocument::getElementsByTagNameNS'
---
# DOMDocument::getElementsByTagNameNS

(PHP 5, PHP 7, PHP 8)

DOMDocument::getElementsByTagNameNS — Шукає всі елементи із заданим ім'ям у вказаному просторі імен

### Опис

```methodsynopsis
public DOMDocument::getElementsByTagNameNS(?string $namespace, string $localName): DOMNodeList
```

Повертає об'єкт [DOMNodeList](class.domnodelist.md) з усіма елементами із заданим локальним ім'ям та URI простору імен.

### Список параметрів

`namespace`

URI простір імен. Спеціальне значення `*` відповідає всім просторам імен.

`localName`

Локальне ім'я елементів, що шукаються. Спеціальне значення `*` відповідає всім локальним іменам.

### Значення, що повертаються

Новий об'єкт класу [DOMNodeList](class.domnodelist.md)містить всі знайдені елементи.

### список змін

| Версия | Описание |
| --- | --- |
|  | `namespace` тепер допускає значення null. |

### Приклади

**Приклад #1 Отримання всіх елементів XInclude**

```php
<?php

$xml = <<<EOD
<?xml version="1.0" ?>
<chapter xmlns:xi="http://www.w3.org/2001/XInclude">
<title>Books of the other guy..</title>
<para>
 <xi:include href="book.xml">
  <xi:fallback>
   <error>xinclude: book.xml not found</error>
  </xi:fallback>
 </xi:include>
 <include>
  This is another namespace
 </include>
</para>
</chapter>
EOD;
$dom = new DOMDocument;

// загрузить XML-строку, определённую выше
$dom->loadXML($xml);

foreach ($dom->getElementsByTagNameNS('http://www.w3.org/2001/XInclude', '*') as $element) {
    echo 'локальное имя: ', $element->localName, ', префикс: ', $element->prefix, "\n";
}
?>
```

Результат виконання цього прикладу:

```
локальное имя: include, префикс: xi
локальное имя: fallback, префикс: xi
```

### Дивіться також

-   [DOMDocument::getElementsByTagName()](domdocument.getelementsbytagname.md) - Шукає всі елементи із заданим локальним ім'ям
