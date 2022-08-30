Реєстрація PHP-функцій як функцій XPath

-   [« DOMXPath::registerNamespace](domxpath.registernamespace.md)
    
-   [Функции DOM »](ref.dom.md)
    
-   [PHP Manual](index.md)
    
-   [DOMXPath](class.domxpath.md)
    
-   Реєстрація PHP-функцій як функцій XPath
    

# DOMXPath::registerPhpFunctions

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DOMXPath::registerPhpFunctions — Реєстрація PHP-функцій як функцій XPath

### Опис

```methodsynopsis
public DOMXPath::registerPhpFunctions(string|array|null $restrict = null): void
```

Цей метод дозволяє використовувати PHP-функції у виразах XPath.

### Список параметрів

`restrict`

Використовуйте цей параметр, щоб дозволити використання лише певних функцій у виразах XPath.

Цей параметр може мати тип string (ім'я функції) або array (масив імен функцій).

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

У таких прикладах використовується файл book.xml, який містить таке:

**Приклад #1 book.xml**

PHP Basics Jim Smith Jane Smith PHP Secrets Jenny Smythe XML basics Joe Black

**Приклад #2 **DOMXPath::registerPHPFunctions()** з `php:functionString`**

```php
<?php
$doc = new DOMDocument;
$doc->load('book.xml');

$xpath = new DOMXPath($doc);

// Регистрация PHP: пространство имён (обязательно)
$xpath->registerNamespace("php", "http://php.net/xpath");

// Регистрация функций PHP (без ограничений)
$xpath->registerPHPFunctions();

// Вызов функции substr для названия книги
$nodes = $xpath->query('//book[php:functionString("substr", title, 0, 3) = "PHP"]');

echo "Найдены {$nodes->length} книги, начинающиеся с 'PHP':\n";
foreach ($nodes as $node) {
    $title  = $node->getElementsByTagName("title")->item(0)->nodeValue;
    $author = $node->getElementsByTagName("author")->item(0)->nodeValue;
    echo "$title автора $author\n";
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Найдены 2 книги, начинающиеся с 'PHP':
PHP Basics автора Jim Smith
PHP Secrets автора Jenny Smythe
```

**Приклад #3 **DOMXPath::registerPHPFunctions()** з `php:function`**

```php
<?php
$doc = new DOMDocument;
$doc->load('book.xml');

$xpath = new DOMXPath($doc);

// Регистрация PHP: пространство имён (обязательно)
$xpath->registerNamespace("php", "http://php.net/xpath");

// Регистрация PHP-функций (только has_multiple)
$xpath->registerPHPFunctions("has_multiple");

function has_multiple($nodes) {
    // Возвращает true, если более одного автора
    return count($nodes) > 1;
}
// Фильтр книг с двумя и более авторами
$books = $xpath->query('//book[php:function("has_multiple", author)]');

echo "Книги с двумя и более авторами:\n";
foreach ($books as $book) {
    echo $book->getElementsByTagName("title")->item(0)->nodeValue . "\n";
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Книги с двумя и более авторами:
PHP Basics
```

### Дивіться також

-   [DOMXPath::registerNamespace()](domxpath.registernamespace.md) - Реєструє простір імен з об'єктом DOMXPath
-   [DOMXPath::query()](domxpath.query.md) - Виконує заданий вираз XPath
-   [DOMXPath::evaluate()](domxpath.evaluate.md) - Обчислює переданий вираз XPath і повертає типізований результат, якщо можливо