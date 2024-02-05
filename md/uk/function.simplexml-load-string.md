---
navigation:
  - function.simplexml-load-file.md: « simplexml\_load\_file
  - book.wddx.md: WDDX »
  - index.md: PHP Manual
  - ref.simplexml.md: Функції SimpleXML
title: simplexml\_load\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# simplexml\_load\_string

(PHP 5, PHP 7, PHP 8)

simplexml\_load\_string — Інтерпретує рядок з XML в об'єкт

### Опис

```methodsynopsis
simplexml_load_string(    string $data,    ?string $class_name = SimpleXMLElement::class,    int $options = 0,    string $namespace_or_prefix = "",    bool $is_prefix = false): SimpleXMLElement|false
```

Отримує правильно сформований XML-рядок і повертає його як об'єкт.

### Список параметрів

`data`

Правильно сформований XML-рядок

`class_name`

Ви можете використовувати цей необов'язковий параметр, щоб функція **simplexml\_load\_string()** повертала об'єкт вказаного класу. Цей клас має розширювати клас [SimpleXMLElement](class.simplexmlelement.md)

`options`

[Побітове АБО (`OR`) .](language.operators.bitwise.md) [констант опцій libxml](libxml.constants.md)

`namespace_or_prefix`

Префікс простору імен або URI.

`is_prefix`

**`true`**, якщо `namespace_or_prefix` є префіксом, та **`false`**, если URI; по умолчанию равен\*\*`false`\*\*

### Значення, що повертаються

Повертає об'єкт (object) класу [SimpleXMLElement](class.simplexmlelement.md) з властивостями, що містять дані, що зберігаються всередині XML-документа або \*\*`false`\*\*в случае возникновения ошибки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Помилки

Генерирует сообщение об ошибке уровня\*\*`E_WARNING`\*\* для кожної помилки, знайденої в даних XML.

**Підказка**

Используйте функцию[libxml\_use\_internal\_errors()](function.libxml-use-internal-errors.md) для того, щоб придушити всі помилки XML, та функцію [libxml\_get\_errors()](function.libxml-get-errors.md)для прохода по ним впоследствии.

### Приклади

**Приклад #1 Інтерпретація рядка XML**

```php
<?php
$string = <<<XML
<?xml version='1.0'?>
<document>
 <title>Что 40?</title>
 <from>Джо</from>
 <to>Джейн</to>
 <body>
  Я знаю, что это - ответ. В чем заключается вопрос?
 </body>
</document>
XML;

$xml = simplexml_load_string($string);

print_r($xml);
?>
```

Результат виконання наведеного прикладу:

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

Тут можна використати `$xml->body`и т.д.

### Дивіться також

-   [simplexml\_load\_file()](function.simplexml-load-file.md) \- Інтерпретує файл XML в об'єкт
-   [SimpleXMLElement::\_\_construct()](simplexmlelement.construct.md) \- Створення нового об'єкта SimpleXMLElement
-   [Робота з помилками XML](simplexml.examples-errors.md)
-   [libxml\_use\_internal\_errors()](function.libxml-use-internal-errors.md) \- Відключення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві
-   [Базове використання SimpleXML](simplexml.examples-basic.md)
