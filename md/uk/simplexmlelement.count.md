---
navigation:
  - simplexmlelement.construct.md: '« SimpleXMLElement::construct'
  - simplexmlelement.getdocnamespaces.md: 'SimpleXMLElement::getDocNamespaces »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::count'
---
# SimpleXMLElement::count

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SimpleXMLElement::count — Підраховує кількість дочірніх елементів у поточного елемента

### Опис

```methodsynopsis
public SimpleXMLElement::count(): int
```

Цей метод підраховує кількість дочірніх елементів поточного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість елементів поточного елемента.

### Приклади

**Приклад #1 Підрахунок кількості дочірніх елементів**

```php
<?php
$xml = <<<EOF
<people>
 <person name="Человек 1">
  <child/>
  <child/>
  <child/>
 </person>
 <person name="Человек 2">
  <child/>
  <child/>
  <child/>
  <child/>
  <child/>
 </person>
</people>
EOF;

$elem = new SimpleXMLElement($xml);

foreach ($elem as $person) {
    printf("%s имеет %d детей.\n", $person['name'], $person->count());
}
?>
```

Результат виконання цього прикладу:

```
Человек 1 имеет 3 детей.
Человек 2 имеет 5 детей.
```

### Дивіться також

-   [SimpleXMLElement::children()](simplexmlelement.children.md) - Знаходить дочірні елементи цього вузла
