---
navigation:
  - language.errors.php7.md: « Помилки в PHP 7
  - language.exceptions.extending.md: Спадкування винятків »
  - index.md: PHP Manual
  - langref.md: Довідник мови
title: Винятки
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Винятки

## Зміст

-   [Спадкування винятків](language.exceptions.extending.md)

У PHP реалізовано модель винятків, аналогічну тим, що використовуються в інших мовах програмування. Виняток у PHP може бути викинуто ([`throw`](language.exceptions.md)) і спіймано (`catch`). Код може бути укладений у блок [`try`](language.exceptions.md), щоб полегшити обробку потенційних винятків. У кожного блоку [`try`](language.exceptions.md) має бути як мінімум один відповідний блок `catch`или`finally`

Якщо викинутий виняток, а в поточній області видимості функції немає блоку `catch`, виняток буде "підніматися" по стеку викликів до зухвалої функції, доки не знайде відповідний блок `catch`. Усі блоки `finally`, які зустрінуться на цьому шляху, будуть виконані. Якщо стек викликів розгортається до глобальної області видимості, не зустрічаючи відповідного блоку `catch`, програма завершується з невиправною помилкою, якщо не було встановлено глобальний обробник винятків.

Викинутий об'єкт повинен наслідувати ([`instanceof`](language.operators.type.md)) інтерфейс [Throwable](class.throwable.md). Спроба викинути об'єкт, який не є таким, призведе до непоправної помилки PHP.

Починаючи з PHP 8.0.0, ключове слово [`throw`](language.exceptions.md) є виразом і може бути використаний у будь-якому контексті виразу. У попередніх версіях воно було твердженням і мало розташовуватися в окремому рядку.

## `catch`

Блок`catch` визначає, як реагувати на викинутий виняток. Блок `catch` визначає один або декілька типів винятків або помилок, які він може обробити, і, за бажанням, змінну, якій можна привласнити виняток (вказівка ​​змінної була обов'язковою до версії PHP 8.0.0). Перший блок `catch`, з яким зіткнеться викинутий виняток чи помилка і відповідає типу викинутого об'єкта, обробить об'єкт.

Декілька блоків `catch` можуть бути використані для перехоплення різних класів винятків. Нормальне виконання (коли виняток не викинуто у блоці [`try`](language.exceptions.md)) будет продолжаться после последнего блока`catch`, Визначеного в послідовності. Винятки можуть бути викинуті ([`throw`](language.exceptions.md)) (або повторно викинуті) усередині блоку `catch`. В іншому випадку виконання буде продовжено після блоку `catch`, який був викликаний.

При виникненні виключення, код, який слідує за твердженням, не буде виконаний, а PHP спробує знайти перший відповідний блок `catch`. . Якщо виняток не спіймано, буде видана помилка PHP з повідомленням "`Uncaught Exception ...`", якщо обробник не був визначений за допомогою функції [set\_exception\_handler()](function.set-exception-handler.md)

Починаючи з версії PHP 7.1.0, у блоці `catch` можна вказувати кілька винятків, використовуючи символ . Це корисно, коли різні винятки із різних ієрархій класів обробляються однаково.

Починаючи з версії PHP 8.0.0, ім'я змінної для упійманого виключення є необов'язковим. Якщо воно не вказано, блок `catch` буде виконано, але не матиме доступу до викинутого об'єкта.

## `finally`

Блок`finally` також може бути вказаний після або замість блоків `catch`. Код у блоці `finally` завжди виконуватиметься після блоків [`try`](language.exceptions.md)и`catch`незалежно від того, чи було викинуто виняток і до відновлення нормального виконання.

Одна з помітних взаємодій відбувається між блоком `finally` та оператором [`return`](function.return.md). Якщо оператор [`return`](function.return.md) зустрічається усередині блоків [`try`](language.exceptions.md)или`catch`, блок`finally` все одно буде виконано. Більше того, оператор [`return`](function.return.md) виконається, коли зустрінеться, але результат буде повернутий після виконання блоку `finally`. Крім того, якщо блок `finally` також містить оператор [`return`](function.return.md), возвращается значение из блока`finally`

## Глобальний обробник винятків

Якщо виключення дозволено поширюватися на глобальну область видимості, це може бути перехоплено глобальним обробником винятків, якщо він встановлено. Функція [set\_exception\_handler()](function.set-exception-handler.md) може встановити функцію, яка буде викликана замість блоку `catch`, якщо не буде викликано жодного іншого блоку. Ефект по суті такий самий, як якби вся програма була обгорнута в блок [`try`](language.exceptions.md)\-`catch` з цією функцією як `catch`

## Примітки

> **Зауваження** :
> 
> Внутрішні функції PHP переважно використовують [звіт про помилки](errorfunc.configuration.md#ini.error-reporting), тільки сучасні [об'єктно-орієнтовані](language.oop5.md) модулі використовують винятки. Однак помилки можна легко перевести у винятки за допомогою класу [ErrorException](class.errorexception.md). Однак ця техніка працює тільки з помилками, що виправляються.
> 
> **Приклад #1 Перетворення звітів про помилки на виключення**
> 
> ```php
> <?php
> function exceptions_error_handler($severity, $message, $filename, $lineno) {
>     throw new ErrorException($message, 0, $severity, $filename, $lineno);
> }
> 
> set_error_handler('exceptions_error_handler');
> ?>
> ```

**Підказка**

Библиотека[Стандартна бібліотека PHP (SPL)](intro.spl.md) надає велику кількість [вбудованих винятків](spl.exceptions.md)

## Приклади

**Приклад #2 Викидання винятку**

```php
<?php
function inverse($x) {
    if (!$x) {
        throw new Exception('Деление на ноль.');
    }
    return 1/$x;
}

try {
    echo inverse(5) . "\n";
    echo inverse(0) . "\n";
} catch (Exception $e) {
    echo 'Выброшено исключение: ',  $e->getMessage(), "\n";
}

// Продолжение выполнения
echo "Привет, мир\n";
?>
```

Результат виконання наведеного прикладу:

```
0.2
Выброшено исключение: Деление на ноль.
Привет, мир
```

**Приклад #3 Обработка исключений с помощью блока`finally`**

```php
<?php
function inverse($x) {
    if (!$x) {
        throw new Exception('Деление на ноль.');
    }
    return 1/$x;
}

try {
    echo inverse(5) . "\n";
} catch (Exception $e) {
    echo 'Поймано исключение: ',  $e->getMessage(), "\n";
} finally {
    echo "Первый блок finally.\n";
}

try {
    echo inverse(0) . "\n";
} catch (Exception $e) {
    echo 'Поймано исключение: ',  $e->getMessage(), "\n";
} finally {
    echo "Второй блок finally.\n";
}

// Продолжение нормального выполнения
echo "Привет, мир\n";
?>
```

Результат виконання наведеного прикладу:

```
0.2
Первый блок finally.
Поймано исключение: Деление на ноль.
Второй блок finally.
Привет, мир
```

**Приклад #4 Взаємодія між блоками `finally`и[`return`](function.return.md)**

```php
<?php

function test() {
    try {
        throw new Exception('foo');
    } catch (Exception $e) {
        return 'catch';
    } finally {
        return 'finally';
    }
}

echo test();
?>
```

Результат виконання наведеного прикладу:

```
finally
```

**Приклад #5 Вкладені винятки**

```php
<?php

class MyException extends Exception { }

class Test {
    public function testing() {
        try {
            try {
                throw new MyException('foo!');
            } catch (MyException $e) {
                // повторный выброс исключения
                throw $e;
            }
        } catch (Exception $e) {
            var_dump($e->getMessage());
        }
    }
}

$foo = new Test;
$foo->testing();

?>
```

Результат виконання наведеного прикладу:

```
string(4) "foo!"
```

**Приклад #6 Обробка кількох винятків в одному блоці catch**

```php
<?php

class MyException extends Exception { }

class MyOtherException extends Exception { }

class Test {
    public function testing() {
        try {
            throw new MyException();
        } catch (MyException | MyOtherException $e) {
            var_dump(get_class($e));
        }
    }
}

$foo = new Test;
$foo->testing();

?>
```

Результат виконання наведеного прикладу:

```
string(11) "MyException"
```

**Приклад #7 Приклад блока`catch` без вказівки змінної**

Допустимо починаючи з PHP 8.0.0

```php
<?php

class SpecificException extends Exception {}

function test() {
    throw new SpecificException('Ой!');
}

try {
    test();
} catch (SpecificException) {
    print "Было поймано исключение SpecificException, но нам безразлично, что у него внутри.";
}
?>
```

**Приклад #8 Throw як вираз**

Допустимо починаючи з PHP 8.0.0

```php
<?php

function test() {
    do_something_risky() or throw new Exception('Всё сломалось');
}

try {
    test();
} catch (Exception $e) {
    print $e->getMessage();
}
?>
```
