---
navigation:
  - simplexmlelement.savexml.md: '« SimpleXMLElement::saveXML'
  - simplexmlelement.valid.md: 'SimpleXMLElement::valid »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::\_\_function toString() { \[native code\] }

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SimpleXMLElement::\_\_toString — Повертає вміст рядка

### Опис

```methodsynopsis
public SimpleXMLElement::__toString(): string
```

Повертає вміст рядка безпосередньо в елементі. Чи не повертає текстовий контент дочірніх елементів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст рядка у разі успішного виконання та порожній рядок в іншому випадку.

### Приклади

**Приклад #1 Отримати вміст рядка**

```php
<?php
$xml = new SimpleXMLElement('<a>1 <b>2 </b>3</a>');
echo $xml;
?>
```

Результат виконання наведеного прикладу:

```
1 3
```

### Дивіться також

-   [SimpleXMLElement::asXML()](simplexmlelement.asxml.md) \- Повертає сформований XML-документ у вигляді рядка на основі елемента SimpleXML
