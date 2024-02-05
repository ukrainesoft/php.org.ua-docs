---
navigation:
  - simplexmlelement.construct.md: '« SimpleXMLElement::\_\_construct'
  - simplexmlelement.current.md: 'SimpleXMLElement::current »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::count

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SimpleXMLElement::count — Підраховує кількість дочірніх елементів у поточного елемента

### Опис

```methodsynopsis
public SimpleXMLElement::count(): int
```

Цей метод підраховує кількість дочірніх елементів поточного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість елементів у поточного елемента.

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

Результат виконання наведеного прикладу:

```
Человек 1 имеет 3 детей.
Человек 2 имеет 5 детей.
```

### Дивіться також

-   [SimpleXMLElement::children()](simplexmlelement.children.md) \- Знаходить дочірні елементи цього вузла
