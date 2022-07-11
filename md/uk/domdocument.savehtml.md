- [« DOMDocument::save](domdocument.save.md)
- [DOMDocument::saveHTMLFile »](domdocument.savehtmlfile.md)

- [PHP Manual](index.md)
- [DOMDocument](class.domdocument.md)
- Зберігає документ із внутрішнього подання до рядка, використовуючи
форматування HTML

# DOMDocument::saveHTML

(PHP 5, PHP 7, PHP 8)

DOMDocument::saveHTML — Зберігає документ із внутрішньої вистави
у рядок, використовуючи форматування HTML

### Опис

public **DOMDocument::saveHTML**(?[DOMNode](class.domnode.md) `$node`
= **`null`**): string\|false

Створює HTML-документ із уявлення DOM. Цю функцію зазвичай викликають
після побудови нового DOM-документа, як показано на прикладі нижче.

### Список параметрів

`node`
Необов'язковий аргумент для виведення підмножини документа.

### Значення, що повертаються

Повертає HTML або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Збереження HTML-дерева у вигляді рядка**

` <?php$doc = new DOMDocument('1.0');$root = $doc->createElement('html');$root = $doc->appendChild($root);$head = $doc->createElement ('head');$head = $root->appendChild($head);$title = $doc->createElement('title');$title = $head->appendChild($title);$text = $ doc->createTextNode('Це заголовок');$text = $title->appendChild($text);echo $doc->saveHTML();?> `

### Дивіться також

- [DOMDocument::saveHTMLFile()](domdocument.savehtmlfile.md) -
Зберігає документ із внутрішнього представлення у файл, використовуючи
форматування HTML
- [DOMDocument::loadHTML()](domdocument.loadhtml.md) - Завантаження HTML
з рядка
- [DOMDocument::loadHTMLFile()](domdocument.loadhtmlfile.md) -
Завантаження HTML із файлу
