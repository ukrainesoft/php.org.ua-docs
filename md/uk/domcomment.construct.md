- [«DOMComment](class.domcomment.md)
- [DOMDocument »](class.domdocument.md)

- [PHP Manual](index.md)
- [DOMComment](class.domcomment.md)
- Створює новий екземпляр класу DOMComment

# DOMComment::\_\_construct

(PHP 5, PHP 7, PHP 8)

DOMComment::\_\_construct — Створює новий екземпляр класу DOMComment

### Опис

public **DOMComment::\_\_construct**(string `$data` = "")

Створює новий об'єкт класу [DOMComment](class.domcomment.md). Об'єкт
буде доступний лише читання. Його можна додати до документа, але
додаткові вузли не можна додавати до об'єкта, доки він не буде
приєднано до документа. Щоб створити записуваний вузол, використовуйте
[DOMDocument::createComment](domdocument.createcomment.md).

### Список параметрів

`data`
Значення коментаря.

### Приклади

**Приклад #1 Створення об'єкту DOMComment**

` <?php$dom = new DOMDocument('1.0', 'iso-8859-1');$element = $dom->appendChild(new DOMElement('root'));$comment = $element->appendChild( new DOMComment('root comment'));echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?><root><!--root comment--></root> */?> `

### Дивіться також

- [DOMDocument::createComment()](domdocument.createcomment.md) -
Створити новий вузол коментаря
