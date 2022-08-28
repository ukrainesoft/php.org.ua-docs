Повертає вміст рядка

-   [« SimpleXMLElement::saveXML](simplexmlelement.savexml.html)
    
-   [SimpleXMLElement::xpath »](simplexmlelement.xpath.html)
    
-   [PHP Manual](index.html)
    
-   [SimpleXMLElement](class.simplexmlelement.html)
    
-   Повертає вміст рядка
    

# SimpleXMLElement::toString

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SimpleXMLElement::toString — Повертає вміст рядка

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
$xml = new SimpleXMLElement('<a>1 <b>2 </b>3</a>');
echo $xml;
?>
```

Результат виконання цього прикладу:

```
1 3
```

### Дивіться також

-   [SimpleXMLElement::asXML()](simplexmlelement.asxml.html) - Повертає сформований XML-документ у вигляді рядка на основі елемента SimpleXML