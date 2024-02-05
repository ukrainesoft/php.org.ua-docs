---
navigation:
  - simplexmlelement.asxml.md: '« SimpleXMLElement::asXML'
  - simplexmlelement.children.md: 'SimpleXMLElement::children »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::attributes'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::attributes

(PHP 5, PHP 7, PHP 8)

SimpleXMLElement::attributes — Повертає атрибути елемента

### Опис

```methodsynopsis
public SimpleXMLElement::attributes(?string $namespaceOrPrefix = null, bool $isPrefix = false): ?SimpleXMLElement
```

Ця функція повертає назви та значення атрибутів, визначені у XML-тегу.

> **Зауваження**: SimpleXML містить правило додавання ітеративних властивостей до більшості методів. Вони не можуть бути переглянуті з використанням [var\_dump()](function.var-dump.md) чи будь-яких інших засобів аналізу об'єктів.

### Список параметрів

`namespaceOrPrefix`

Необов'язковий простір імен для отримання атрибутів

`isPrefix`

По умолчанию\*\*`false`\*\*

### Значення, що повертаються

Повертає об'єкт, що ітерується. [SimpleXMLElement](class.simplexmlelement.md), яким можна переміщатися для перебору всіх атрибутів тега.

Повертає **`null`**, якщо викликаний об'єкт [SimpleXMLElement](class.simplexmlelement.md) вже представляє атрибут, а чи не тег.

### Приклади

**Приклад #1 Інтерпретація рядка XML**

```php
<?php
$string = <<<XML
<a>
 <foo name="one" game="lonely">1</foo>
</a>
XML;

$xml = simplexml_load_string($string);
foreach($xml->foo[0]->attributes() as $a => $b) {
    echo $a,'="',$b,"\"\n";
}
?>
```

Результат виконання наведеного прикладу:

```
name="one"
game="lonely"
```

### Дивіться також

-   [Базове використання SimpleXML](simplexml.examples-basic.md)
