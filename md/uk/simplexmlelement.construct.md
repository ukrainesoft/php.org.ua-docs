---
navigation:
  - simplexmlelement.children.md: '« SimpleXMLElement::children'
  - simplexmlelement.count.md: 'SimpleXMLElement::count »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::construct'
---
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

Створює новий об'єкт [SimpleXMLElement](class.simplexmlelement.md)

### Список параметрів

`data`

Правильно сформований XML-рядок. Може бути шляхом або URL до XML-документа, якщо параметр `dataIsURL` встановлений в **`true`**

`options`

Необов'язковий параметр використовується для вказівки [додаткових параметрів Libxml](libxml.constants.md)які впливають на читання документів XML. Параметри, які впливають на виведення документів XML (наприклад, **`LIBXML_NOEMPTYTAG`**), ігноруються.

> **Зауваження**
> 
> Для доступу до глибоко вкладених елементів XML або для обробки дуже великих текстових вузлів може знадобитися використовувати **`[LIBXML_PARSEHUGE](libxml.constants.md#constant.libxml-parsehuge)`**

`dataIsURL`

За замовчуванням `dataIsURL` встановлений в **`false`**. Використовуйте **`true`** для вказівки того, що `data` є шляхом або URL до документа XML замість даних типу string.

`namespaceOrPrefix`

Префікс простору імен або URI.

`isPrefix`

**`true`**, якщо `namespaceOrPrefix` є префіксом, \*\*`false`\*\*якщо це URI; за замовчуванням **`false`**

### Помилки

Видає повідомлення з помилкою **`E_WARNING`** для кожної знайденої помилки в XML-даних, та додатково генерує виняток [Exception](class.exception.md)якщо дані XML не можуть бути розібрані.

**Підказка**

Використовуйте [libxmluseinternalerrors()](function.libxml-use-internal-errors.md) для придушення всіх XML-помилок та [libxmlgeterrors()](function.libxml-get-errors.md) для їхньої ітерації за ними.

### Приклади

> **Зауваження**
> 
> Перелічені приклади можуть містити `example.php`, в якому визначається XML-рядок, розташована в першому прикладі посібника з [базовому использованию](simplexml.examples-basic.md)

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

-   [Базовое использование SimpleXML](simplexml.examples-basic.md)
-   [simplexmlloadstring()](function.simplexml-load-string.md) - Інтерпретує рядок з XML в об'єкт
-   [simplexmlloadfile()](function.simplexml-load-file.md) - Інтерпретує файл XML в об'єкт
-   [Робота з помилками XML](simplexml.examples-errors.md)
-   [libxmluseinternalerrors()](function.libxml-use-internal-errors.md) - Відключення помилок libxml та передача повноважень щодо вибірки та обробки інформації про помилки користувачеві
-   [libxmlsetstreamscontext()](function.libxml-set-streams-context.md) - Встановлення контексту потоків для наступного завантаження чи запису документа за допомогою libxml
