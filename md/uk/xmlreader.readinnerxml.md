Вийняти XML із поточного вузла

-   [« XMLReader::read](xmlreader.read.html)
    
-   [XMLReader::readOuterXml »](xmlreader.readouterxml.html)
    
-   [PHP Manual](index.html)
    
-   [XMLReader](class.xmlreader.html)
    
-   Вийняти XML із поточного вузла
    

# XMLReader::readInnerXml

(PHP 5> = 5.2.0, PHP 7, PHP 8)

XMLReader::readInnerXml — Вийняти XML із поточного вузла

### Опис

```methodsynopsis
public XMLReader::readInnerXml(): string
```

Читає вміст поточного вузла, включаючи дочірні вузли та розмітку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст поточного вузла у вигляді рядка. Порожній рядок повертається у разі виникнення помилки.

### Примітки

**Застереження**

Ця функція доступна лише якщо PHP скомпільовано за допомогою libxml 20620 або старше.

### Дивіться також

-   [XMLReader::readString()](xmlreader.readstring.html) - Прочитати вміст поточного вузла як рядок
-   [XMLReader::readOuterXml()](xmlreader.readouterxml.html) - Отримати XML із поточного вузла, включаючи сам вузол
-   [XMLReader::expand()](xmlreader.expand.html) - Повернути копію поточного вузла у вигляді об'єкта DOM