Інтерпретує рядок з XML в об'єкт

-   [« simplexmlloadfile](function.simplexml-load-file.html)
    
-   [WDDX »](book.wddx.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SimpleXML](ref.simplexml.html)
    
-   Інтерпретує рядок з XML в об'єкт
    

# simplexmlloadstring

(PHP 5, PHP 7, PHP 8)

simplexmlloadstring — Інтерпретує рядок з XML в об'єкт

### Опис

```methodsynopsis
simplexml_load_string(    string $data,    ?string $class_name = SimpleXMLElement::class,    int $options = 0,    string $namespace_or_prefix = "",    bool $is_prefix = false): SimpleXMLElement|false
```

Отримує правильно сформований XML-рядок і повертає його як об'єкт.

### Список параметрів

`data`

Правильно сформований XML-рядок

`class_name`

Ви можете використовувати цей необов'язковий параметр, щоб функція **simplexmlloadstring()** повертала об'єкт вказаного класу. Цей клас має розширювати клас [SimpleXMLElement](class.simplexmlelement.html)

`options`

Починаючи з Libxml 2.6.0, ви можете також використовувати параметр `options`, щоб вказати [дополнительные параметры Libxml](libxml.constants.html)

`namespace_or_prefix`

Префікс простору імен або URI.

`is_prefix`

**`true`**, якщо `namespace_or_prefix` є префіксом, та \*\*`false`\*\*якщо URI; за умовчанням дорівнює **`false`**

### Значення, що повертаються

Повертає об'єкт (object) класу [SimpleXMLElement](class.simplexmlelement.html) з властивостями, що містять дані, що зберігаються всередині XML-документа або **`false`** у разі виникнення помилки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### Помилки

Генерує повідомлення про помилку рівня **`E_WARNING`** для кожної помилки, знайденої в даних XML.

**Підказка**

Використовуйте функцію [libxmluseinternalerrors()](function.libxml-use-internal-errors.html) для того, щоб придушити всі помилки XML, та функцію [libxmlgeterrors()](function.libxml-get-errors.html) для проходу ними згодом.

### Приклади

**Приклад #1 Інтерпретація рядка XML**

```php
<?php
$string = <<<XML
<?xml version='1.0'?>
<document>
 <title>Что 40?</title>
 <from>Джо</from>
 <to>Джейн</to>
 <body>
  Я знаю, что это - ответ. В чем заключается вопрос?
 </body>
</document>
XML;

$xml = simplexml_load_string($string);

print_r($xml);
?>
```

Результат виконання цього прикладу:

```
SimpleXMLElement Object
(
  [title] => Что 40?
  [from] => Джо
  [to] => Джейн
  [body] =>
   Я знаю, что это - ответ. В чем заключается вопрос?
)
```

Тут можна використати `$xml->body` і т.д.

### Дивіться також

-   [simplexmlloadfile()](function.simplexml-load-file.html) - Інтерпретує файл XML в об'єкт
-   [SimpleXMLElement::construct()](simplexmlelement.construct.html) - Створення нового об'єкта SimpleXMLElement
-   [Робота з помилками XML](simplexml.examples-errors.html)
-   [libxmluseinternalerrors()](function.libxml-use-internal-errors.html) - Відключення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві
-   [Базовое использование SimpleXML](simplexml.examples-basic.html)