Базове використання SimpleXML

-   [« Приклади](simplexml.examples.html)
    
-   [Робота з помилками XML »](simplexml.examples-errors.html)
    
-   [PHP Manual](index.html)
    
-   [Приклади](simplexml.examples.html)
    
-   Базове використання SimpleXML
    

## Базове використання SimpleXML

Деякі приклади цього посібника включають рядок XML. Замість того, щоб повторювати її в кожному прикладі, покладіть цей рядок у файл, який включайте в кожному прикладі. Цей рядок наведено у наступному прикладі. Крім цього, можна створити XML-документ і зчитувати його функцією [simplexmlloadfile()](function.simplexml-load-file.html)

**Приклад #1 Файл example.php з рядком XML**

```php
<?php
$xmlstr = <<<XML
<?xml version='1.0' standalone='yes'?>
<movies>
 <movie>
  <title>PHP: Появление Парсера</title>
  <characters>
   <character>
    <name>Ms. Coder</name>
    <actor>Onlivia Actora</actor>
   </character>
   <character>
    <name>Mr. Coder</name>
    <actor>El Act&#211;r</actor>
   </character>
  </characters>
  <plot>
   Таким образом, это язык. Это всё равно язык программирования. Или
   это скриптовый язык? Все раскрывается в этом документальном фильме,
   похожем на фильм ужасов.
  </plot>
  <great-lines>
   <line>PHP решает все мои проблемы в вебе</line>
  </great-lines>
  <rating type="thumbs">7</rating>
  <rating type="stars">5</rating>
 </movie>
</movies>
XML;
?>
```

SimpleXML користуватися дуже просто! Спробуйте отримати якийсь рядок чи число з базового документа XML.

**Приклад #2 Отримання частини документа `<plot>`**

```php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

echo $movies->movie[0]->plot;
?>
```

Результат виконання цього прикладу:

```
Таким образом, это язык. Это всё равно язык программирования. Или
   это скриптовый язык? Все раскрывается в этом документальном фильме,
   похожем на фильм ужасов.
```

У PHP отримати доступ до елемента в XML документі, що містить у назві неприпустимі символи (наприклад, дефіс), можна шляхом укладання цього імені елемента у фігурні дужки та апострофи.

**Приклад #3 Отримання рядка `<line>`**

```php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

echo $movies->movie->{'great-lines'}->line;
?>
```

Результат виконання цього прикладу:

```
PHP решает все мои проблемы в вебе
```

**Приклад #4 Доступ до неунікальних елементів SimpleXML**

Якщо існує кілька екземплярів дочірніх елементів в одному батьківському елементі, то потрібно застосовувати стандартні методи ітерації.

```php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

/* Для каждого узла <character>, мы отдельно выведем имя <name>. */
foreach ($movies->movie->characters->character as $character) {
   echo $character->name, ' играет ', $character->actor, PHP_EOL;
}

?>
```

Результат виконання цього прикладу:

```
Ms. Coder играет Onlivia Actora
Mr. Coder играет El ActÓr
```

> **Зауваження**
> 
> Властивості (`$movies->movie` у попередньому прикладі) не є масивами. Це [ітерований](class.iterator.html) об'єкт [у вигляді масиву](class.arrayaccess.html)

**Приклад #5 Використання атрибутів**

Досі ми лише отримували назви та значення елементів. SimpleXML може також отримати доступ до атрибутів елемента. Отримати доступ до атрибуту елемента можна так само, як і до елементів масиву (array).

```php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

/* Доступ к узлу <rating> первого фильма.
 * Так же выведем шкалу оценок. */
foreach ($movies->movie[0]->rating as $rating) {
    switch((string) $rating['type']) { // Получение атрибутов элемента по индексу
    case 'thumbs':
        echo $rating, ' thumbs up';
        break;
    case 'stars':
        echo $rating, ' stars';
        break;
    }
}
?>
```

Результат виконання цього прикладу:

```
7 thumbs up5 stars
```

**Приклад #6 Порівняння елементів та атрибутів з текстом**

Для порівняння елемента або атрибута з рядком або для передачі в функцію як текст, необхідно привести його до рядка, використовуючи `(string)`. В іншому випадку, PHP розглядатиме елемент як об'єкт.

```php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

if ((string) $movies->movie->title == 'PHP: Появление Парсера') {
    print 'Мой любимый фильм.';
}

echo htmlentities((string) $movies->movie->title);
?>
```

Результат виконання цього прикладу:

```
Мой любимый фильм.PHP: Появление Парсера
```

**Приклад #7 Порівняння двох елементів**

Два елементи SimpleXMLElements вважаються різними, навіть якщо вони вказують на той самий об'єкт.

```php
<?php
include 'example.php';

$movies1 = new SimpleXMLElement($xmlstr);
$movies2 = new SimpleXMLElement($xmlstr);
var_dump($movies1 == $movies2); // false
?>
```

Результат виконання цього прикладу:

```
bool(false)
```

**Приклад #8 Використання XPath**

SimpleXML включає вбудовану підтримку XPath. Пошук усіх елементів `<character>`

```php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

foreach ($movies->xpath('//character') as $character) {
    echo $character->name, ' играет ', $character->actor, PHP_EOL;
}
?>
```

`//`' служить як шаблон. Для вказівки абсолютного шляху опустіть одну з косих рис.

Результат виконання цього прикладу:

```
Ms. Coder играет Onlivia Actora
Mr. Coder играет by El ActÓr
```

**Приклад #9 Встановлення значень**

Дані SimpleXML не обов'язково повинні бути незмінними. Об'єкт дозволяє маніпулювати всіма елементами.

```php
<?php
include 'example.php';
$movies = new SimpleXMLElement($xmlstr);

$movies->movie[0]->characters->character[0]->name = 'Miss Coder';

echo $movies->asXML();
?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0" standalone="yes"?>
<movies>
 <movie>
  <title>PHP: Появление Парсера</title>
  <characters>
   <character>
    <name>Miss Coder</name>
    <actor>Onlivia Actora</actor>
   </character>
   <character>
    <name>Mr. Coder</name>
    <actor>El Act&#xD3;r</actor>
   </character>
  </characters>
  <plot>
   Таким образом, это язык. Это всё равно язык программирования. Или
   это скриптовый язык? Все раскрывается в этом документальном фильме,
   похожем на фильм ужасов.
  </plot>
  <great-lines>
   <line>PHP решает все мои задачи в web</line>
  </great-lines>
  <rating type="thumbs">7</rating>
  <rating type="stars">5</rating>
 </movie>
</movies>
```

**Приклад #10 Додавання елементів та атрибутів**

SimpleXML має можливість легко додавати дочірні елементи та атрибути.

```php
<?php
include 'example.php';
$movies = new SimpleXMLElement($xmlstr);

$character = $movies->movie[0]->characters->addChild('character');
$character->addChild('name', 'Mr. Parser');
$character->addChild('actor', 'John Doe');

$rating = $movies->movie[0]->addChild('rating', 'PG');
$rating->addAttribute('type', 'mpaa');

echo $movies->asXML();
?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0" standalone="yes"?>
<movies>
 <movie>
  <title>PHP: Появление Парсера</title>
  <characters>
   <character>
    <name>Ms. Coder</name>
    <actor>Onlivia Actora</actor>
   </character>
   <character>
    <name>Mr. Coder</name>
    <actor>El Act&#xD3;r</actor>
   </character>
  <character><name>Mr. Parser</name><actor>John Doe</actor></character></characters>
  <plot>
   Таким образом, это язык. Это всё равно язык программирования. Или
   это скриптовый язык? Все раскрывается в этом документальном фильме,
   похожем на фильм ужасов.
  </plot>
  <great-lines>
   <line>PHP решает все мои задачи в web</line>
  </great-lines>
  <rating type="thumbs">7</rating>
  <rating type="stars">5</rating>
 <rating type="mpaa">PG</rating></movie>
</movies>
```

**Приклад #11 Взаємодія з DOM**

PHP може перетворювати XML-вузли з SimpleXML у формат DOM і навпаки. Цей приклад показує, як можна змінити DOM-елемент у SimpleXML.

```php
<?php
$dom = new DOMDocument;
$dom->loadXML('<books><book><title>чепуха</title></book></books>');
if (!$dom) {
    echo 'Ошибка при разборе документа';
    exit;
}

$books = simplexml_import_dom($dom);

echo $books->book[0]->title;
?>
```

Результат виконання цього прикладу:

```
чепуха
```