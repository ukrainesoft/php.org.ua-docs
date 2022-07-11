- [« SimpleXMLElement::addAttribute](simplexmlelement.addattribute.md)
- [SimpleXMLElement::asXML »](simplexmlelement.asxml.md)

- [PHP Manual](index.md)
- [SimpleXMLElement](class.simplexmlelement.md)
- Додає дочірній елемент до сайту XML

# SimpleXMLElement::addChild

(PHP 5 \>= 5.1.3, PHP 7, PHP 8)

SimpleXMLElement::addChild — Додає дочірній елемент до сайту XML

### Опис

public **SimpleXMLElement::addChild**(string `$qualifiedName`, ?string
`$value` = **`null`**, ?string `$namespace` = **`null`**):
?[SimpleXMLElement](class.simplexmlelement.md)

Додає дочірній елемент до вузла та повертає нащадка SimpleXMLElement.

### Список параметрів

`qualifiedName`
Ім'я дочірнього елемента, що додається.

`value`
Якщо вказано, значення (вміст) дочірнього елемента.

`namespace`
Якщо зазначено, то простір імен, до якого належить дочірній
елемент.

### Значення, що повертаються

Метод `addChild` повертає об'єкт
[SimpleXMLElement](class.simplexmlelement.md), що представляє
доданого нащадка до вузла XML у разі успішного виконання;
**`null`** у разі виникнення помилки.

### Приклади

> **Примітка**:
>
> Перелічені приклади можуть містити "example.php", в якому
> визначається XML-рядок, розташована в першому прикладі посібника з
> [базове використання](simplexml.examples-basic.md).

**Приклад #1 Додавання атрибутів та нащадків до елемента SimpleXML**

` <?phpinclude 'example.php';$sxe = new SimpleXMLElement($xmlstr);$sxe->addAttribute('type', 'documentary');$movie = $sxe->addChild('movie');$ movie->addChild('title', 'PHP2: Історії парсера');$movie->addChild('plot', 'Всі про людей, створювали його.');$characters = $movie->addChild(' );$character = $characters->addChild('character');$character->addChild('name', 'Mr. Parser');$character->addChild('actor', 'John Doe');$ rating =$movie->addChild('rating', '5');$rating->addAttribute('type', 'stars');echo $sxe->asXML();?> `

Результатом виконання цього прикладу буде щось подібне:

<?xml version="1.0" standalone="yes"?>
<movies type="documentary">
<movie>
<title>PHP: Поява Парсера</title>
<characters>
<character>
<name>Ms. Coder</name>
<actor>Onlivia Actora</actor>
</character>
<character>
<name>Mr. Coder</name>
<actor>El ActÓr</actor>
</character>
</characters>
<plot>
Отже, це мова. Це все одно мова програмування. Або
це скриптова мова? Все розкривається у цьому документальному фільмі,
схожим на фільм жахів.
</plot>
<great-lines>
<line>PHP вирішує всі мої завдання на web</line>
</great-lines>
<rating type="thumbs">7</rating>
<rating type="stars">5</rating>
</movie>
<movie>
<title>PHP2: Історії парсера</title>
<plot>Все про людей, які його створювали.</plot>
<characters>
<character>
<name>Mr. Parser</name>
<actor>John Doe</actor>
</character>
</characters>
<rating type="stars">5</rating>
</movie>
</movies>

### Дивіться також

- [SimpleXMLElement::addAttribute()](simplexmlelement.addattribute.md) -
Додає атрибут до SimpleXML-елементу
- [Базове використання SimpleXML](simplexml.examples-basic.md)
