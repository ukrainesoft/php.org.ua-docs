Інтерпретує файл XML в об'єкт

-   [« simplexml\_import\_dom](function.simplexml-import-dom.html)
    
-   [simplexml\_load\_string »](function.simplexml-load-string.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SimpleXML](ref.simplexml.html)
    
-   Інтерпретує файл XML в об'єкт
    

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

Ви можете використовувати цей необов'язковий параметр, щоб функція **simplexmlloadfile()** повертала об'єкт вказаного класу. Цей клас має розширювати клас [SimpleXMLElement](class.simplexmlelement.html)

`options`

Починаючи з Libxml 2.6.0, ви можете також використовувати параметр `options`, щоб вказати [дополнительные параметры Libxml](libxml.constants.html)

`namespace_or_prefix`

Префікс простору імен або URI.

`is_prefix`

**`true`**, якщо `namespace_or_prefix` є префіксом, та **`false`**якщо URI; за умовчанням дорівнює **`false`**

### Значення, що повертаються

Повертає об'єкт (object) класу [SimpleXMLElement](class.simplexmlelement.html) з властивостями, що містять дані, що зберігаються всередині XML-документа або **`false`** у разі виникнення помилки.

**Увага**

Ця функція може повертати як логічне значення **`false`**так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### Помилки

Генерує повідомлення про помилку рівня **`E_WARNING`** для кожної помилки, знайденої в даних XML.

**Підказка**

Використовуйте функцію [libxml\_use\_internal\_errors()](function.libxml-use-internal-errors.html) для того, щоб придушити всі помилки XML, та функцію [libxml\_get\_errors()](function.libxml-get-errors.html) для проходу ними згодом.

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

-   [simplexml\_load\_string()](function.simplexml-load-string.html) - Інтерпретує рядок з XML в об'єкт
-   [SimpleXMLElement::\_\_construct()](simplexmlelement.construct.html) - Створення нового об'єкта SimpleXMLElement
-   [Работа с ошибками XML](simplexml.examples-errors.html)
-   [libxml\_use\_internal\_errors()](function.libxml-use-internal-errors.html) - Відключення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві
-   [Базовое использование SimpleXML](simplexml.examples-basic.html)
-   [libxml\_set\_streams\_context()](function.libxml-set-streams-context.html) - Встановлення контексту потоків для наступного завантаження або запису документа за допомогою libxml