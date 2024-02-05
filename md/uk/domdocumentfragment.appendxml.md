---
navigation:
  - domdocumentfragment.append.md: '« DOMDocumentFragment::append'
  - domdocumentfragment.construct.md: 'DOMDocumentFragment::\_\_construct »'
  - index.md: PHP Manual
  - class.domdocumentfragment.md: DOMDocumentFragment
title: 'DOMDocumentFragment::appendXML'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocumentFragment::appendXML

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

DOMDocumentFragment::appendXML — Додавання необроблених даних XML

### Опис

```methodsynopsis
public DOMDocumentFragment::appendXML(string $data): bool
```

Додає необроблені дані XML в об'єкт класу DOMDocumentFragment.

Цей метод не є частиною стандарту DOM. Він був розроблений для спрощення процедури додавання XML DocumentFragment до DOMDocument.

Якщо ви хочете дотримуватись стандарту, вам потрібно буде створити тимчасовий DOMDocument з фіктивним коренем, а потім пройти по всіх вузлах нащадкам кореневого вузла XML-документа, щоб додати їх.

### Список параметрів

`data`

XML для додавання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Додавання XML-даних у документ**

```php
<?php
$doc = new DOMDocument();
$doc->loadXML("<root/>");
$f = $doc->createDocumentFragment();
$f->appendXML("<foo>text</foo><bar>text2</bar>");
$doc->documentElement->appendChild($f);
echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<root><foo>text</foo><bar>text2</bar></root>
```
