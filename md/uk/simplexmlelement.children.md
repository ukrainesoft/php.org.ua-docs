Знаходить дочірні елементи цього вузла

-   [« SimpleXMLElement::attributes](simplexmlelement.attributes.md)
    
-   [SimpleXMLElement::construct »](simplexmlelement.construct.md)
    
-   [PHP Manual](index.md)
    
-   [SimpleXMLElement](class.simplexmlelement.md)
    
-   Знаходить дочірні елементи цього вузла
    

# SimpleXMLElement::children

(PHP 5, PHP 7, PHP 8)

SimpleXMLElement::children — Знаходить дочірні елементи цього сайту

### Опис

```methodsynopsis
public SimpleXMLElement::children(?string $namespaceOrPrefix = null, bool $isPrefix = false): ?SimpleXMLElement
```

Цей метод знаходить усі дочірні елементи вузла. Результат підкоряється стандартним правилам ітерації.

> **Зауваження**: SimpleXML містить правило додавання ітеративних властивостей до більшості методів. Вони не можуть бути переглянуті з використанням [vardump()](function.var-dump.html) чи будь-яких інших засобів аналізу об'єктів.

### Список параметрів

`namespaceOrPrefix`

Необов'язковий простір імен XML.

`isPrefix`

Якщо `isPrefix` встановлений в **`true`** `namespaceOrPrefix` буде розглянуто як префікс. Якщо **`false`** `namespaceOrPrefix` буде розглянуто як простір імен URL.

### Значення, що повертаються

Повертає елемент [SimpleXMLElement](class.simplexmlelement.md)навіть якщо вузол не має дочірніх елементів, якщо вузол не представляє атрибут, у цьому випадку функція повертає **`null`**

### Приклади

**Приклад #1 Обхід псевдомасиву `children()`**

```php
<?php
$xml = new SimpleXMLElement(
'<person>
 <child role="сын">
  <child role="дочь"/>
 </child>
 <child role="дочь">
  <child role="сын">
   <child role="сын"/>
  </child>
 </child>
</person>');

foreach ($xml->children() as $second_gen) {
    echo ' У человека родился(-ась) ' . $second_gen['role'];

    foreach ($second_gen->children() as $third_gen) {
        echo ', у которого родился(-ась) ' . $third_gen['role'] . ';';

        foreach ($third_gen->children() as $fourth_gen) {
            echo ' и у ' . $third_gen['role'] .
                ' родился(-ась) ' . $fourth_gen['role'];
        }
    }
}
?>
```

Результат виконання цього прикладу:

```
У человека родился(-ась) сын, у которого родился(-ась) дочь; У человека
родился(-ась) дочь, у которого родился(-ась) сын; и у сын родился(-ась) сын
```

**Приклад #2 Використання простору імен**

```php
<?php
$xml = '<example xmlns:foo="my.foo.urn">
  <foo:a>Яблоко</foo:a>
  <foo:b>Банан</foo:b>
  <c>Вишня</c>
</example>';

$sxe = new SimpleXMLElement($xml);

$kids = $sxe->children('foo');
var_dump(count($kids));

$kids = $sxe->children('foo', TRUE);
var_dump(count($kids));

$kids = $sxe->children('my.foo.urn');
var_dump(count($kids));

$kids = $sxe->children('my.foo.urn', TRUE);
var_dump(count($kids));

$kids = $sxe->children();
var_dump(count($kids));
?>
```

```
int(0)
int(2)
int(2)
int(0)
int(1)
```

### Дивіться також

-   [SimpleXMLElement::count()](simplexmlelement.count.md) - Підраховує кількість дочірніх елементів у поточного елемента
-   [count()](function.count.md) - Підраховує кількість елементів масиву або Countable об'єкті