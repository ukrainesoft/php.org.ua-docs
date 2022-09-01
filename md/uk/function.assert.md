---
navigation:
  - function.assert-options.html: « assertoptions
  - function.cli-get-process-title.html: cligetprocesstitle »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: assert
---
# assert

(PHP 4, PHP 5, PHP 7, PHP 8)

assert — Перевіряє, чи є затвердження **`false`**

### Опис

PHP 5 та 7

```methodsynopsis
assert(mixed $assertion, string $description = ?): bool
```

PHP 7

```methodsynopsis
assert(mixed $assertion, Throwable $exception = ?): bool
```

**assert()** перевірить задане твердження `assertion` і здійснить відповідну дію, якщо результатом перевірки виявиться **`false`**

#### Традиційна робота функції assert (PHP 5 та 7)

Якщо `assertion` задається у вигляді рядка, воно розглядатиметься функцією **assert()** як PHP-код. Якщо ви передасте як параметр `assertion` логічний вираз, то цей вираз не відображатиметься як параметр для функції затвердження, заданої за допомогою [assertoptions()](function.assert-options.html). Цей вираз буде перетворено на рядок перед викликом функції обробника, а у випадку **`false`** буде використано порожній рядок.

Затвердження повинні використовуватися лише з метою налагодження. Їх можна використовувати для тестування якихось умов, які у штатних ситуаціях завжди набувають значення **`true`**, зворотне повинне вказувати на програмні помилки. Також їх можна використовувати, щоб переконатися у наявності будь-яких модулів або системних обмежень.

Затвердження не повинні використовуватись у звичайних операціях, таких як перевірка вхідних параметрів. Як правило, скрипт повинен коректно виконуватись, якщо вимкнути перевірку тверджень.

Поведінка функції **assert()** можна змінювати за допомогою функції [assertoptions()](function.assert-options.html) або встановленням .ini-налаштувань.

Функція [assertoptions()](function.assert-options.html) та/або директива **`ASSERT_CALLBACK`** дозволяють задати callback-функцію, яка буде викликатись при провалі перевірки затвердження.

Можливість викликати callback-функції з **assert()** може бути корисною для створення автоматизованих тестових пакетів. За допомогою цих функцій можна отримати код, переданий на перевірку разом з інформацією про те, де ця перевірка була здійснена. Подібну інформацію можна отримати й іншими методами, проте використання тверджень швидше та простіше.

Callback-функція має приймати три аргументи. Перший аргумент має містити файл, у якому твердження не пройшло перевірку. Другий аргумент відповідає за номер рядка у цьому файлі. У третьому аргументі передаватиметься вираз, що містить помилку (якщо таких кілька, рядкові значення, на кшталт 1 чи "два" не будуть передаватися через цей аргумент). Користувачі PHP версій 5.4.8 та вище можуть задати четвертий необов'язковий аргумент `description`, який буде також передано у функцію **assert()**

#### Очікування (тільки PHP 7)

У PHP 7 **assert()** - це мовна конструкція, що дозволяє визначати очікування: твердження, які працюють у середовищі розробки та тестування, але з метою оптимізації відключені на продуктовому оточенні.

У той час як функція [assertoptions()](function.assert-options.html) може бути використана для контролю над поведінкою програми описаним вище чином, для зворотної сумісності, але в PHP 7 код повинен використовувати дві нові конфігураційні директиви для управління поведінкою **assert()** і не викликати функції [assertoptions()](function.assert-options.html)

**Конфігураційні директиви PHP 7 для функції **assert()****

| Директива | Значение по умолчанию | Возможные значения |
| --- | --- | --- |
| [zend.assertions](ini.core.html#ini.zend.assertions) | `1` |  |

-   `1`: генерує та виконує код (режим розробки)
-   `0`: генерує код, але перестрибує через нього під час виконання
-   `-1`: не генерує код (робочий режим)

[assert.exception](info.configuration.html#ini.assert.exception) `0`

-   `1`: викидає виняток, коли твердження зазнає невдачі, класу, наданого у параметрі `exception`, або класу [AssertionError](class.assertionerror.md), якщо параметр `exception` не передано.
-   `0`: використовує або створює екземпляр класу [Throwable](class.throwable.md) як описано вище, але тільки генерує попередження на основі цього об'єкта, не викидаючи його (для сумісності з поведінкою PHP 5)

### Список параметрів

`assertion`

Твердження. PHP 5 може бути рядком (string) для виконання або логічним значенням (bool) для перевірки. У PHP 7 це також може бути будь-який вираз, який повертає значення, яке буде виконано, і результат використаний для визначення успішності перевірки.

**Увага**

Використання рядка (string) у параметрі `assertion` оголошено *Застарілим* з PHP 7.2 та *ВИДАЛЕНО*починаючи з PHP 8.0.0.

`description`

Необов'язковий опис, який буде додано до повідомлення, якщо перевірка затвердження `assertion` буде провалено. У PHP 7 використовується опис за замовчуванням (якщо його не було передано), де буде вказано сам виклик **assert()**

`exception`

У PHP 7 другий параметр може бути об'єктом [Throwable](class.throwable.md) замість рядка (string). Цей об'єкт буде викидатися у разі невдалої перевірки затвердження при включеній конфігураційній директиві [assert.exception](info.configuration.html#ini.assert.exception)

### Значення, що повертаються

**`false`**, якщо перевірку провалено, **`true`** в іншому випадку.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція **assert()** більше не буде оцінювати строкові аргументи, натомість вони розглядатимуться як будь-який інший аргумент. Замість `assert($a == $b)` слід використовувати `assert('$a == $b')`. Директива `assert.quiet_eval` php.ini та константа **`ASSERT_QUIET_EVAL`** також були видалені, оскільки вони не мають сенсу. |
|  | Оголошення функції з ім'ям `assert()` всередині простору імен тепер заборонено та викликає **`E_COMPILE_ERROR`** |
|  | Оголошення функції з ім'ям `assert()` всередині простору імен оголошено застарілим. Таке оголошення тепер видає помилку рівня **`E_DEPRECATED`** |
|  | Використання рядків у параметрі `assertion` оголошено застарілим і призводитиме до помилок рівня **`E_DEPRECATED`** у разі, коли і [assert.active](info.configuration.html#ini.assert.active) і [zend.assertions](ini.core.html#ini.zend.assertions) встановлені у значення `1` |
|  | **assert()** тепер мовна конструкція, а не функція . `assertion` тепер може бути виразом. Другий параметр тепер інтерпретується як виняток `exception` (якщо передано об'єкт [Throwable](class.throwable.md)), або як опис `description`, що підтримується з версії PHP 5.4.8 і далі. |

### Приклади

#### Традиційна робота функції assert (PHP 5 та 7)

**Приклад #1 Обробка невдалих перевірок тверджень із використанням власного оброблювача**

```php
<?php
// Активация утверждений и отключение вывода ошибок
assert_options(ASSERT_ACTIVE, 1);
assert_options(ASSERT_WARNING, 0);
assert_options(ASSERT_QUIET_EVAL, 1);

// Создание обработчика
function my_assert_handler($file, $line, $code)
{
    echo "<hr>Неудачная проверка утверждения:
        Файл '$file'<br />
        Строка '$line'<br />
        Код '$code'<br /><hr />";
}

// Подключение callback-функции
assert_options(ASSERT_CALLBACK, 'my_assert_handler');

// Выполнение проверки утверждения, которое завершится неудачей
assert('mysql_query("")');
?>
```

**Приклад #2 Використання власного оброблювача з виводом опису**

```php
<?php
// Активация утверждений и отключение вывода ошибок
assert_options(ASSERT_ACTIVE, 1);
assert_options(ASSERT_WARNING, 0);
assert_options(ASSERT_QUIET_EVAL, 1);

// Создание обработчика
function my_assert_handler($file, $line, $code, $desc = null)
{
    echo "Неудачная проверка утверждения в $file:$line: $code";
    if ($desc) {
        echo ": $desc";
    }
    echo "\n";
}

// Подключение callback-функции
assert_options(ASSERT_CALLBACK, 'my_assert_handler');

// Выполнение проверки утверждения, которое завершится неудачей
assert('2 < 1');
assert('2 < 1', 'Два больше чем один');
?>
```

Результат виконання цього прикладу:

```
Неудачная проверка утверждения в test.php:21: 2 < 1
 Неудачная проверка утверждения в test.php:22: 2 < 1: Два больше чем один
```

#### Очікування (тільки PHP 7)

**Приклад #3 Очікування без винятку**

```php
<?php
assert(true == false);
echo 'Привет!';
?>
```

При директиві [zend.assertions](ini.core.html#ini.zend.assertions), встановленою в 0, цей код виведе:

```
Привет!
```

При директивах [zend.assertions](ini.core.html#ini.zend.assertions), встановленої в 1 та [assert.exception](info.configuration.html#ini.assert.exception), встановленою в 0, даний приклад виведе:

```
Warning: assert(): assert(true == false) failed in - on line 2
Привет!
```

При директивах [zend.assertions](ini.core.html#ini.zend.assertions), встановленої в 1 та [assert.exception](info.configuration.html#ini.assert.exception), встановленої в 1, цей код виведе:

```
Fatal error: Uncaught AssertionError: assert(true == false) in -:2
Stack trace:
#0 -(2): assert(false, 'assert(true == ...')
#1 {main}
  thrown in - on line 2
```

**Приклад #4 Очікування з власним винятком**

```php
<?php
class CustomError extends AssertionError {}

assert(true == false, new CustomError('True не является false!'));
echo 'Привет!';
?>
```

При директиві [zend.assertions](ini.core.html#ini.zend.assertions), встановленою в 0, цей код виведе:

```
Привет!
```

При директивах [zend.assertions](ini.core.html#ini.zend.assertions), встановленої в 1 та [assert.exception](info.configuration.html#ini.assert.exception), встановленою в 0, цей код виведе:

```
Warning: assert(): CustomError: True не является false! in -:4
Stack trace:
#0 {main} failed in - on line 4
Привет!
```

При директивах [zend.assertions](ini.core.html#ini.zend.assertions), встановленої в 1 та [assert.exception](info.configuration.html#ini.assert.exception), встановленої в 1, цей код виведе:

```
Fatal error: Uncaught CustomError: True не является false! in -:4
Stack trace:
#0 {main}
  thrown in - on line 4
```

### Дивіться також

-   [assertoptions()](function.assert-options.html) - Встановлення та отримання налаштувань механізму перевірки тверджень
