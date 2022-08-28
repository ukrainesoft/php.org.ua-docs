Прочитати вміст поточного вузла як рядок

-   [« XMLReader::readOuterXml](xmlreader.readouterxml.html)
    
-   [XMLReader::setParserProperty »](xmlreader.setparserproperty.html)
    
-   [PHP Manual](index.html)
    
-   [XMLReader](class.xmlreader.html)
    
-   Прочитати вміст поточного вузла як рядок
    

# XMLReader::readString

(PHP 5> = 5.2.0, PHP 7, PHP 8)

XMLReader::readString — Прочитати вміст поточного вузла як рядок

### Опис

```methodsynopsis
public XMLReader::readString(): string
```

Читає вміст поточного вузла як рядок.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст поточного вузла у вигляді рядка. У разі виникнення помилки рядок буде порожнім.

### Примітки

**Застереження**

Ця функція доступна лише якщо PHP скомпільовано за допомогою libxml 20620 або старше.

### Дивіться також

-   [XMLReader::readOuterXml()](xmlreader.readouterxml.html) - Отримати XML із поточного вузла, включаючи сам вузол
-   [XMLReader::readInnerXml()](xmlreader.readinnerxml.html) - Вийняти XML із поточного вузла
-   [XMLReader::expand()](xmlreader.expand.html) - Повернути копію поточного вузла у вигляді об'єкта DOM