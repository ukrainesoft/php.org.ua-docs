---
navigation:
  - domdocument.normalizedocument.html: '« DOMDocument::normalizeDocument'
  - domdocument.relaxngvalidate.html: 'DOMDocument::relaxNGValidate »'
  - index.html: PHP Manual
  - class.domdocument.html: DOMDocument
title: 'DOMDocument::registerNodeClass'
---
# DOMDocument::registerNodeClass

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DOMDocument::registerNodeClass — Реєстрація розширеного класу, який використовується для створення типу базового вузла

### Опис

```methodsynopsis
public DOMDocument::registerNodeClass(string $baseClass, ?string $extendedClass): bool
```

Цей метод дозволяє зареєструвати свій власний розширений клас DOM, який згодом використовуватиметься модулем PHP DOM.

Цей метод не є частиною стандарту DOM.

### Список параметрів

`baseClass`

Клас DOM, який ви бажаєте розширити. Список таких класів можна побачити у [введении](book.dom.html)

`extendedClass`

Ім'я розширеного класу. Якщо передати **`null`**, будуть видалені всі раніше зареєстровані класи, які розширюють базовий клас `baseClass`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Додавання нового методу до класу DOMElement для спрощення коду**

```php
<?php

class myElement extends DOMElement {
   function appendElement($name) {
      return $this->appendChild(new myElement($name));
   }
}

class myDocument extends DOMDocument {
   function setRoot($name) {
      return $this->appendChild(new myElement($name));
   }
}

$doc = new myDocument();
$doc->registerNodeClass('DOMElement', 'myElement');

// С этих пор добавление одного элемента к другому
// требует всего одного вызова метода!
$root = $doc->setRoot('root');
$child = $root->appendElement('child');
$child->setAttribute('foo', 'bar');

echo $doc->saveXML();

?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0"?>
<root><child foo="bar"/></root>
```

**Приклад #2 Отримання елементів у вигляді класу користувача**

```php
<?php
class myElement extends DOMElement {
    public function __toString() {
        return $this->nodeValue;
    }
}

$doc = new DOMDocument;
$doc->loadXML("<root><element><child>text in child</child></element></root>");
$doc->registerNodeClass("DOMElement", "myElement");

$element = $doc->getElementsByTagName("child")->item(0);
var_dump(get_class($element));

// Воспользуемся __toString методом..
echo $element;
?>
```

Результат виконання цього прикладу:

```
string(9) "myElement"
text in child
```

**Приклад #3 Отримання імені документа власника**

Коли створюється екземпляр розширеного класу [DOMDocument](class.domdocument.html), властивість ownerDocument посилатиметься на створюваний об'єкт. Однак, якщо видалити всі посилання на цей клас, він буде знищений, а замість нього буде створено новий об'єкт [DOMDocument](class.domdocument.html). З цієї причини ви можете використати функцію **DOMDocument::registerNodeClass()** стосовно об'єкту [DOMDocument](class.domdocument.html)

```php
<?php
class MyDOMDocument extends DOMDocument {
}

class MyOtherDOMDocument extends DOMDocument {
}

// Создаём MyDOMDocument с некоторым XML-содержимым
$doc = new MyDOMDocument;
$doc->loadXML("<root><element><child>text in child</child></element></root>");

$child = $doc->getElementsByTagName("child")->item(0);

// Текущий владелец узла - MyDOMDocument
var_dump(get_class($child->ownerDocument));

// Уничтожаем MyDOMDocument
unset($doc);

// И создаём новый экземпляр DOMDocument
var_dump(get_class($child->ownerDocument));

// Импортируем узел из MyDOMDocument
$newdoc = new MyOtherDOMDocument;
$child = $newdoc->importNode($child);

// Регистрируем пользовательский DOMDocument
$newdoc->registerNodeClass("DOMDocument", "MyOtherDOMDocument");

var_dump(get_class($child->ownerDocument));
unset($doc);

// Новый владелец узла изменился на MyOtherDOMDocument
var_dump(get_class($child->ownerDocument));
?>
```

Результат виконання цього прикладу:

```
string(13) "MyDOMDocument"
string(11) "DOMDocument"
string(18) "MyOtherDOMDocument"
string(18) "MyOtherDOMDocument"
```

**Приклад #4 Об'єкти користувача тимчасові**

**Застереження**

Об'єкти зареєстрованих класів вузлів є тимчасовими, тобто. вони знищуються, коли на них більше не посилаються з PHP-коду і відтворюються при повторному вилученні. Це означає, що значення властивостей, що настроюються, будуть втрачені після відновлення.

```php
<?php
class MyDOMElement extends DOMElement
{
    public $myProp = 'значение по умолчанию';
}

$doc = new DOMDocument();
$doc->registerNodeClass('DOMElement', 'MyDOMElement');

$node = $doc->createElement('a');
$node->myProp = 'изменённое значение';
$doc->appendChild($node);

echo $doc->childNodes[0]->myProp, PHP_EOL;
unset($node);
echo $doc->childNodes[0]->myProp, PHP_EOL;
?>
```

Результат виконання цього прикладу:

```
изменённое значение
значение по умолчанию
```
