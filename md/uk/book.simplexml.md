---
navigation:
  - function.libxml-use-internal-errors.md: « libxml\_use\_internal\_errors
  - intro.simplexml.md: Вступ "
  - index.md: PHP Manual
  - refs.xml.md: Обробка XML
title: SimpleXML
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXML

-   [Вступ](intro.simplexml.md)
-   [Встановлення та налаштування](simplexml.setup.md)
    -   [Вимоги](simplexml.requirements.md)
    -   [Установка](simplexml.installation.md)
    -   [Налаштування під час виконання](simplexml.configuration.md)
    -   [Типи ресурсів](simplexml.resources.md)
-   [Обумовлені константи](simplexml.constants.md)
-   [Приклади](simplexml.examples.md)
    -   [Базове використання SimpleXML](simplexml.examples-basic.md)
    -   [Робота з помилками XML](simplexml.examples-errors.md)
-   [SimpleXMLElement](class.simplexmlelement.md) \- Клас SimpleXMLElement
    -   [SimpleXMLElement::addAttribute](simplexmlelement.addattribute.md) \- Додає атрибут до SimpleXML-елементу
    -   [SimpleXMLElement::addChild](simplexmlelement.addchild.md)— Додає дочірній елемент до сайту XML
    -   [SimpleXMLElement::asXML](simplexmlelement.asxml.md)— Повертає сформований XML-документ у вигляді рядка на основі елемента SimpleXML
    -   [SimpleXMLElement::attributes](simplexmlelement.attributes.md)— Повертає атрибути елемента
    -   [SimpleXMLElement::children](simplexmlelement.children.md)— Знаходить дочірні елементи цього вузла
    -   [SimpleXMLElement::\_\_construct](simplexmlelement.construct.md)— Створення нового об'єкта SimpleXMLElement
    -   [SimpleXMLElement::count](simplexmlelement.count.md)— Підраховує кількість дочірніх елементів у поточного елемента
    -   [SimpleXMLElement::current](simplexmlelement.current.md)— Повертає поточний елемент
    -   [SimpleXMLElement::getDocNamespaces](simplexmlelement.getdocnamespaces.md)— Повертає простір імен, оголошених у документі
    -   [SimpleXMLElement::getName](simplexmlelement.getname.md)— Отримує ім'я елемента XML
    -   [SimpleXMLElement::getNamespaces](simplexmlelement.getnamespaces.md)— Повертає простір імен, які використовуються в документі
    -   [SimpleXMLElement::getChildren](simplexmlelement.getchildren.md)— Повертає дочірні елементи поточного елемента
    -   [SimpleXMLElement::hasChildren](simplexmlelement.haschildren.md)— Перевіряє, чи поточний елемент має дочірні елементи.
    -   [SimpleXMLElement::key](simplexmlelement.key.md)— Повертає ім'я XML-тегу поточного елемента
    -   [SimpleXMLElement::next](simplexmlelement.next.md)— Перехід до наступного елементу
    -   [SimpleXMLElement::registerXPathNamespace](simplexmlelement.registerxpathnamespace.md)— Створює префікс/простір імен контексту для наступного запиту XPath
    -   [SimpleXMLElement::rewind](simplexmlelement.rewind.md)— Перемотування до першого елементу
    -   [SimpleXMLElement::saveXML](simplexmlelement.savexml.md) \- Псевдонім SimpleXMLElement::asXML
    -   [SimpleXMLElement::\_\_function toString() { \[native code\] }](simplexmlelement.tostring.md)— Повертає вміст рядка
    -   [SimpleXMLElement::valid](simplexmlelement.valid.md)— Перевіряє, чи поточний елемент є коректним.
    -   [SimpleXMLElement::xpath](simplexmlelement.xpath.md)— Запускає запит XPath до XML-даних
-   [SimpleXMLIterator](class.simplexmliterator.md) \- Клас SimpleXMLIterator
-   [Функції SimpleXML](ref.simplexml.md)
    -   [simplexml\_import\_dom](function.simplexml-import-dom.md)— Отримує об'єкт класу SimpleXMLElement із вузла DOM
    -   [simplexml\_load\_file](function.simplexml-load-file.md)— Інтерпретує файл XML в об'єкт
    -   [simplexml\_load\_string](function.simplexml-load-string.md)— Інтерпретує рядок із XML в об'єкт
