Створення нового об'єкта SimpleXMLElement

-   [« SimpleXMLElement::children](simplexmlelement.children.html)
    
-   [SimpleXMLElement::count »](simplexmlelement.count.html)
    
-   [PHP Manual](index.html)
    
-   [SimpleXMLElement](class.simplexmlelement.html)
    
-   Створення нового об'єкта SimpleXMLElement
    

# SimpleXMLElement::construct

(PHP 5, PHP 7, PHP 8)

SimpleXMLElement::construct — Створення нового об'єкта SimpleXMLElement

### Опис

public **SimpleXMLElement::construct**  
string `$data`  
int `$options`  
bool `$dataIsURL` **`false`**  
string `$namespaceOrPrefix` = "",  
bool `$isPrefix` **`false`**  

Створює новий об'єкт [SimpleXMLElement](class.simplexmlelement.html)

### Список параметрів

`data`

Правильно сформований XML-рядок. Може бути шляхом або URL до XML-документа, якщо параметр `dataIsURL` встановлений в **`true`**

`options`

Необов'язковий параметр використовується для вказівки [дополнительных параметров Libxml](libxml.constants.html)які впливають на читання документів XML. Параметри, які впливають на виведення документів XML (наприклад, **`LIBXML_NOEMPTYTAG`**), ігноруються.

> **Зауваження**
> 
> Для доступу до глибоко вкладених елементів XML або для обробки дуже великих текстових вузлів може знадобитися використовувати **`[LIBXML_PARSEHUGE](libxml.constants.html#constant.libxml-parsehuge)`**

`dataIsURL`

За замовчуванням `dataIsURL` встановлений в **`false`**. Використовуйте **`true`** для вказівки того, що `data` є шляхом або URL до документа XML замість даних типу string.

`namespaceOrPrefix`

Префікс простору імен або URI.

`isPrefix`

**`true`**, якщо `namespaceOrPrefix` є префіксом, **`false`**якщо це URI; за замовчуванням **`false`**

### Помилки

Видає повідомлення з помилкою **`E_WARNING`** для кожної знайденої помилки в XML-даних, та додатково генерує виняток [Exception](class.exception.html)якщо дані XML не можуть бути розібрані.

**Підказка**

Використовуйте [libxml\_use\_internal\_errors()](function.libxml-use-internal-errors.html) для придушення всіх XML-помилок та [libxml\_get\_errors()](function.libxml-get-errors.html) для їхньої ітерації за ними.

### Приклади

> **Зауваження**
> 
> Перелічені приклади можуть містити `example.php`, в якому визначається XML-рядок, розташована в першому прикладі посібника з [базовому использованию](simplexml.examples-basic.html)

**Приклад #1 Створення об'єкта SimpleXMLElement**

```php
<?php

include 'example.php';

$sxe = new SimpleXMLElement($xmlstr);
echo $sxe->movie[0]->title;

?>
```

Результат виконання цього прикладу:

```
PHP: Появление Парсера
```

**Приклад #2 Створення об'єкта SimpleXMLElement з URL**

```php
<?php

$sxe = new SimpleXMLElement('http://example.org/document.xml', NULL, TRUE);
echo $sxe->asXML();

?>
```

### Дивіться також

-   [Базовое использование SimpleXML](simplexml.examples-basic.html)
-   [simplexml\_load\_string()](function.simplexml-load-string.html) - Інтерпретує рядок з XML в об'єкт
-   [simplexml\_load\_file()](function.simplexml-load-file.html) - Інтерпретує файл XML в об'єкт
-   [Работа с ошибками XML](simplexml.examples-errors.html)
-   [libxml\_use\_internal\_errors()](function.libxml-use-internal-errors.html) - Відключення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві
-   [libxml\_set\_streams\_context()](function.libxml-set-streams-context.html) - Встановлення контексту потоків для наступного завантаження чи запису документа за допомогою libxml