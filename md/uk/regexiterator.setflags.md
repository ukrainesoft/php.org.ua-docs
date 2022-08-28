Установка прапорів

-   [« RegexIterator::getRegex](regexiterator.getregex.html)
    
-   [RegexIterator::setMode »](regexiterator.setmode.html)
    
-   [PHP Manual](index.html)
    
-   [RegexIterator](class.regexiterator.html)
    
-   Установка прапорів
    

# RegexIterator::setFlags

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RegexIterator::setFlags — Установка прапорів

### Опис

```methodsynopsis
public RegexIterator::setFlags(int $flags): void
```

Задає прапори налаштування.

### Список параметрів

`flags`

Прапори, бітова маска класу констант.

Нижче наведено доступні прапори. Сенс та значення прапорів описані в розділі [предопределённых констант](class.regexiterator.html#regexiterator.constants)

**Прапори [RegexIterator](class.regexiterator.html)**

| значение | константа                                                                           |
|----------|-------------------------------------------------------------------------------------|
|          | [RegexIterator::USE\_KEY](class.regexiterator.html#regexiterator.constants.use-key) |

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::setFlags()****

Створює новий об'єкт-ітератор, який вибирає елементи, ключі яких починаються зі слова '`test`

```php
<?php
$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/^test/');
$regexIterator->setFlags(RegexIterator::USE_KEY);

foreach ($regexIterator as $key => $value) {
    echo $key . ' => ' . $value . "\n";
}
?>
```

Результат виконання цього прикладу:

```
teststr2 => another test
```

### Дивіться також

-   [RegexIterator::getFlags()](regexiterator.getflags.html) - Отримання прапорів налаштування