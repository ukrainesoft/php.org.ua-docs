Повертає атрибути елемента

-   [« SimpleXMLElement::asXML](simplexmlelement.asxml.html)
    
-   [SimpleXMLElement::children »](simplexmlelement.children.html)
    
-   [PHP Manual](index.html)
    
-   [SimpleXMLElement](class.simplexmlelement.html)
    
-   Повертає атрибути елемента
    

# SimpleXMLElement::attributes

(PHP 5, PHP 7, PHP 8)

SimpleXMLElement::attributes — Повертає атрибути елемента

### Опис

```methodsynopsis
public SimpleXMLElement::attributes(?string $namespaceOrPrefix = null, bool $isPrefix = false): ?SimpleXMLElement
```

Ця функція повертає назви та значення атрибутів, визначені у XML-тегу.

> **Зауваження**: SimpleXML містить правило додавання ітеративних властивостей до більшості методів. Вони не можуть бути переглянуті з використанням [var\_dump()](function.var-dump.html) чи будь-яких інших засобів аналізу об'єктів.

### Список параметрів

`namespaceOrPrefix`

Необов'язковий простір імен для отримання атрибутів

`isPrefix`

За замовчуванням **`false`**

### Значення, що повертаються

Повертає об'єкт, що ітерується. [SimpleXMLElement](class.simplexmlelement.html), яким можна переміщатися для перебору всіх атрибутів тега.

Повертає **`null`**, якщо викликаний об'єкт [SimpleXMLElement](class.simplexmlelement.html) вже представляє атрибут, а чи не тег.

### Приклади

**Приклад #1 Інтерпретація рядка XML**

```php
<?php
$string = <<<XML
<a>
 <foo name="one" game="lonely">1</foo>
</a>
XML;

$xml = simplexml_load_string($string);
foreach($xml->foo[0]->attributes() as $a => $b) {
    echo $a,'="',$b,"\"\n";
}
?>
```

Результат виконання цього прикладу:

```
name="one"
game="lonely"
```

### Дивіться також

-   [Базовое использование SimpleXML](simplexml.examples-basic.html)