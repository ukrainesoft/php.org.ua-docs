- [« RegexIterator::getRegex](regexiterator.getregex.md)
- [RegexIterator::setMode »](regexiterator.setmode.md)

- [PHP Manual](index.md)
- [RegexIterator](class.regexiterator.md)
- Установка прапорів

# RegexIterator::setFlags

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

RegexIterator::setFlags — Установка прапорів

### Опис

public **RegexIterator::setFlags**(int `$flags`): void

Задає прапорці настроювання.

### Список параметрів

`flags`
Прапори, бітова маска класу констант.

Нижче наведені доступні прапори. Сенс та значення прапорів описані в
розділі [передбачених констант](class.regexiterator.md#regexiterator.constants).

| значення | константа                                                                        |
|----------|----------------------------------------------------------------------------------|
| 1        | [RegexIterator::USE_KEY](class.regexiterator.md#regexiterator.constants.use-key) |

**Прапори [RegexIterator](class.regexiterator.md)**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::setFlags()****

Створює новий об'єкт-ітератор, який відбирає елементи, ключі яких
починаються зі слова ''test''.

` <?php$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');$arrayIterator = new Ar $regexIterator==newRegexIterator($arrayIterator, '/^test/');$regexIterator->setFlags(RegexIterator::USE_KEY);foreach ($regexIterator as $key => $ ' => ' . $value . "
";}?> `

Результат виконання цього прикладу:

teststr2 => інший test

### Дивіться також

- [RegexIterator::getFlags()](regexiterator.getflags.md) - Отримання
прапорів налаштування
