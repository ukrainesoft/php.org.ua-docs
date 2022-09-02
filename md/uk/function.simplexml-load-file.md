---
navigation:
  - function.simplexml-import-dom.md: « simplexmlimportdom
  - function.simplexml-load-string.md: simplexmlloadstring »
  - index.md: PHP Manual
  - ref.simplexml.md: Функции SimpleXML
title: simplexmlloadfile
---
# simplexmlloadfile

(PHP 5, PHP 7, PHP 8)

simplexmlloadfile — Інтерпретує файл XML в об'єкт

### Опис

```methodsynopsis
simplexml_load_file(    string $filename,    ?string $class_name = SimpleXMLElement::class,    int $options = 0,    string $namespace_or_prefix = "",    bool $is_prefix = false): SimpleXMLElement|false
```

Перетворює правильно сформований XML-документ у вказаному файлі на об'єкт.

### Список параметрів

`filename`

Шлях до файлу XML

`class_name`

Ви можете використовувати цей необов'язковий параметр, щоб функція **simplexmlloadfile()** повертала об'єкт вказаного класу. Цей клас має розширювати клас [SimpleXMLElement](class.simplexmlelement.md)

`options`

Починаючи з Libxml 2.6.0, ви можете також використовувати параметр `options`, щоб вказати [додаткові параметри Libxml](libxml.constants.md)

`namespace_or_prefix`

Префікс простору імен або URI.

`is_prefix`

**`true`**, якщо `namespace_or_prefix` є префіксом, та \*\*`false`\*\*якщо URI; за умовчанням дорівнює **`false`**

### Значення, що повертаються

Повертає об'єкт (object) класу [SimpleXMLElement](class.simplexmlelement.md) з властивостями, що містять дані, що зберігаються всередині XML-документа або **`false`** у разі виникнення помилки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.md). Використовуйте [оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Помилки

Генерує повідомлення про помилку рівня **`E_WARNING`** для кожної помилки, знайденої в даних XML.

**Підказка**

Використовуйте функцію [libxmluseinternalerrors()](function.libxml-use-internal-errors.md) для того, щоб придушити всі помилки XML, та функцію [libxmlgeterrors()](function.libxml-get-errors.md) для проходу ними згодом.

### Приклади

**Приклад #1 Інтерпретація документа XML**

```php
<?php
// Файл test.xml содержит XML-документ с корневым элементом
// и по меньшей мере элемент /[root]/title.

if (file_exists('test.xml')) {
    $xml = simplexml_load_file('test.xml');

    print_r($xml);
} else {
    exit('Не удалось открыть файл test.xml.');
}
?>
```

Цей скрипт виведе наступне у разі успішного завершення:

```
SimpleXMLElement Object
(
  [title] => Пример заголовка
  ...
)
```

Тут ви можете використати `$xml->title` та будь-які інші елементи.

### Дивіться також

-   [simplexmlloadstring()](function.simplexml-load-string.md) - Інтерпретує рядок з XML в об'єкт
-   [SimpleXMLElement::construct()](simplexmlelement.construct.md) - Створення нового об'єкта SimpleXMLElement
-   [Робота з помилками XML](simplexml.examples-errors.md)
-   [libxmluseinternalerrors()](function.libxml-use-internal-errors.md) - Відключення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві
-   [Базовое использование SimpleXML](simplexml.examples-basic.md)
-   [libxmlsetstreamscontext()](function.libxml-set-streams-context.md) - Встановлення контексту потоків для наступного завантаження або запису документа за допомогою libxml
