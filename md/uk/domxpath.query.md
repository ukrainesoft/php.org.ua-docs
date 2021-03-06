- [« DOMXPath::evaluate](domxpath.evaluate.md)
- [DOMXPath::registerNamespace »](domxpath.registernamespace.md)

- [PHP Manual](index.md)
- [DOMXPath](class.domxpath.md)
- Виконує заданий вираз XPath

# DOMXPath::query

(PHP 5, PHP 7, PHP 8)

DOMXPath::query — Виконує заданий вираз XPath

### Опис

public **DOMXPath::query**(string `$expression`,
?[DOMNode](class.domnode.md) `$contextNode` = **`null`**, bool
`$registerNodeNS` = **`true`**):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Виконує заданий XPath-вираз `expression`.

### Список параметрів

`expression`
Вираз XPath для виконання.

`contextNode`
Додатковий параметр `contextNode` може бути вказаний для виконання
відносних запитів XPath. За замовчуванням запити виконуються
щодо кореневого елемента.

`registerNodeNS`
Додатковий параметр `registerNodeNS` можна вказати, щоб вимкнути
автоматичну реєстрацію контексту вузла.

### Значення, що повертаються

Повертає об'єкт [DOMNodeList](class.domnodelist.md), що містить
вузли, що відповідають виразу XPath `expression`. Будь-який вираз, не
повертає вузли, поверне порожній об'єкт
[DOMNodeList](class.domnodelist.md).

Якщо `expression` побудовано неправильно або `contextNode` має неправильне
значення, **DOMXPath::query()** поверне **`false`**.

### Приклади

**Приклад #1 Отримання списку всіх книг англійською**

` <?php$doc = new DOMDocument;// Не хочемо возитися з пробілами$doc->preserveWhiteSpace = false;$doc->load('book.xml');$xpath = new DOMXPath($doc);// Починаємо з кореневого елемента$query = '//book/chapter/para/informaltable/tgroup/tbody/row/entry[. = "en"]';$entries = $xpath->query($query);foreach ($entries as $entry) {    echo "Знайдено книга {$entry->previousSibling->previousSibling->. " автор {$entry->previousSibling->nodeValue}
";}?> `

Результат виконання цього прикладу:

Знайдена книга The Grapes of Wrath, авторка John Steinbeck
Знайдена книга The Pearl, авторка John Steinbeck

Також можна використовувати параметр `contextNode` для більш короткого
записи виразу:

` <?php$doc = new DOMDocument;$doc->preserveWhiteSpace = false;$doc->load('book.xml');$xpath = new DOMXPath($doc);$tbody =$doc->getElementsByTagName 'tbody')->item(0);// запит щодо вузла tbody$query = 'row/entry[. = "en"]';$entries = $xpath->query($query, $tbody);foreach ($entries as $entry) {    echo "Знайдена книга {$entry->previousSibling-u> " . " автор {$entry->previousSibling->nodeValue}
";}?> `

### Дивіться також

- [DOMXPath::evaluate()](domxpath.evaluate.md) - Обчислює
переданий вираз XPath і повертає типізований результат,
якщо можливо
