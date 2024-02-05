---
navigation:
  - function.simplexml-import-dom.md: « simplexml\_import\_dom
  - function.simplexml-load-string.md: simplexml\_load\_string »
  - index.md: PHP Manual
  - ref.simplexml.md: Функції SimpleXML
title: simplexml\_load\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# simplexml\_load\_file

(PHP 5, PHP 7, PHP 8)

simplexml\_load\_file — Інтерпретує файл XML в об'єкт

### Опис

```methodsynopsis
simplexml_load_file(    string $filename,    ?string $class_name = SimpleXMLElement::class,    int $options = 0,    string $namespace_or_prefix = "",    bool $is_prefix = false): SimpleXMLElement|false
```

Перетворює правильно сформований XML-документ у вказаному файлі об'єкт.

### Список параметрів

`filename`

Шлях до файлу XML

`class_name`

Можна використовувати цей параметр, щоб функція **simplexml\_load\_file()** повертала об'єкт вказаного класу. Цей клас має розширювати клас [SimpleXMLElement](class.simplexmlelement.md)

`options`

[Побітове АБО (`OR`) .](language.operators.bitwise.md) [констант опцій libxml](libxml.constants.md)

`namespace_or_prefix`

Префікс простору імен або URI.

`is_prefix`

**`true`**, если значение параметра`namespace_or_prefix`— префикс, и\*\*`false`**, если URI; по умолчанию равен**`false`\*\*

### Значення, що повертаються

Повертає об'єкт (object) класу [SimpleXMLElement](class.simplexmlelement.md) з властивостями, що містять дані, що зберігаються всередині XML-документа або \*\*`false`\*\*в случае возникновения ошибки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Помилки

Генерирует сообщение об ошибке уровня\*\*`E_WARNING`\*\* для кожної помилки, знайденої в даних XML.

**Підказка**

Используйте функцию[libxml\_use\_internal\_errors()](function.libxml-use-internal-errors.md) для того, щоб придушити всі помилки XML, та функцію [libxml\_get\_errors()](function.libxml-get-errors.md)для прохода по ним впоследствии.

### Приклади

**Приклад #1 Інтерпретація документа XML**

```php
<?php
// Файл test.xml содержит XML-документ с корневым элементом
// и по меньшей мере элемент /[root]/title.

if (file_exists('test.xml')) {
    $xml = simplexml_load_file('test.xml');

    print_r($xml);
} else {
    exit('Не удалось открыть файл test.xml.');
}
?>
```

Цей скрипт виведе наступне у разі успішного завершення:

```
SimpleXMLElement Object
(
  [title] => Приклад заголовка
  ...
)
```

Тут ви можете використати `$xml->title` та будь-які інші елементи.

### Дивіться також

-   [simplexml\_load\_string()](function.simplexml-load-string.md) \- Інтерпретує рядок з XML в об'єкт
-   [SimpleXMLElement::\_\_construct()](simplexmlelement.construct.md) \- Створення нового об'єкта SimpleXMLElement
-   [Робота з помилками XML](simplexml.examples-errors.md)
-   [libxml\_use\_internal\_errors()](function.libxml-use-internal-errors.md) \- Відключення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві
-   [Базове використання SimpleXML](simplexml.examples-basic.md)
-   [libxml\_set\_streams\_context()](function.libxml-set-streams-context.md) \- Встановлення контексту потоків для наступного завантаження чи запису документа за допомогою libxml
