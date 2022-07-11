- [«DOMText](class.domtext.md)
- [DOMText::isElementContentWhitespace »](domtext.iselementcontentwhitespace.md)

- [PHP Manual](index.md)
- [DOMText](class.domtext.md)
- Створює об'єкт класу DOMText

# DOMText::\_\_construct

(PHP 5, PHP 7, PHP 8)

DOMText::\_\_construct — Створює об'єкт класу
[DOMText](class.domtext.md)

### Опис

public **DOMText::\_\_construct**(string `$data` = "")

Створює новий екземпляр класу [DOMText](class.domtext.md).

### Список параметрів

`data`
Значення текстового сайту. Якщо значення не передано, буде створено порожній
текстовий вузол.

### Приклади

**Приклад #1 Створення нового сайту DOMText**

` <?php$dom = new DOMDocument('1.0', 'iso-8859-1');$element = $dom->appendChild(new DOMElement('root'));$text = $element->appendChild( new DOMText('root value'));echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?><root>root value</root> */?> `

### Дивіться також

- [DOMDocument::createTextNode()](domdocument.createtextnode.md) -
Створити новий текстовий вузол
