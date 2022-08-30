Винятки

-   [« Помилки в PHP 7](language.errors.php7.html)
    
-   [Наследование исключений »](language.exceptions.extending.html)
    
-   [PHP Manual](index.html)
    
-   [Справочник языка](langref.html)
    
-   Винятки
    

# Винятки

## Зміст

-   [Наследование исключений](language.exceptions.extending.html)

Модель виключень (exceptions) в PHP схожа з іншими мовами програмування. Виняток можна згенерувати (викинути) за допомогою оператора [`throw`](language.exceptions.html), і можна перехопити (зловити) оператором [`catch`](language.exceptions.html#language.exceptions.catch). Код, що генерує виняток, повинен бути оточений блоком [`try`](language.exceptions.html), щоб можна було перехопити виняток. Кожен блок [`try`](language.exceptions.html) повинен мати щонайменше один відповідний йому блок [`catch`](language.exceptions.html#language.exceptions.catch) або [`finally`](language.exceptions.html#language.exceptions.finally)

Якщо викинуто виняток, для якого немає блоку [`catch`](language.exceptions.html#language.exceptions.catch) в поточній функції, цей виняток буде "випливати" по стеку виклику, поки не буде знайдений відповідний блок [`catch`](language.exceptions.html#language.exceptions.catch). При цьому всі зустрічені блоки [`finally`](language.exceptions.html#language.exceptions.finally) будуть виконані. Якщо стек викликів розкрутиться до глобальної області видимості, не зустрівши відповідного блоку [`catch`](language.exceptions.html#language.exceptions.catch), програма завершить роботу з фатальною помилкою, якщо у вас не налаштований глобальний обробник винятків.

Об'єкт, що генерується, повинен належати класу [Exception](class.exception.html) або успадковуватися від [Exception](class.exception.html). Спроба згенерувати виняток іншого класу призведе до фатальної помилки PHP.

Починаючи з PHP 8.0.0, ключове слово [`throw`](language.exceptions.html) є виразом і може використовуватись у контексті інших виразів. У попередніх версіях воно було оператором і вимагало розміщення в окремому рядку.

### `catch`

Блок [`catch`](language.exceptions.html#language.exceptions.catch) визначає те, як слід реагувати на викинутий виняток. У блоці [`catch`](language.exceptions.html#language.exceptions.catch) вказується один або більше типів винятків або помилок (Error), які він оброблятиме. Також вказується і змінна, якій буде надано спійманий виняток (починаючи з PHP 8.0.0 задавати цю змінну не обов'язково). Викинутий виняток чи помилку буде оброблено першим відповідним блоком [`catch`](language.exceptions.html#language.exceptions.catch)

Можна використовувати декілька блоків [`catch`](language.exceptions.html#language.exceptions.catch), що перехоплюють різні класи винятків. Нормальне виконання (коли не генеруються виключення у блоках [`try`](language.exceptions.html)) буде продовжено за останнім блоком [`catch`](language.exceptions.html#language.exceptions.catch). Винятки можуть бути згенеровані (або викликані ще раз) оператором [`throw`](language.exceptions.html) всередині блоку [`catch`](language.exceptions.html#language.exceptions.catch). Якщо ні, то виконання буде продовжено після відпрацювання блоку [`catch`](language.exceptions.html#language.exceptions.catch)

При генерації виключення код, наступний після виразу, що описується, не буде виконаний, а PHP спробує знайти перший блок [`catch`](language.exceptions.html#language.exceptions.catch), що перехоплює виняток цього класу. Якщо виняток не буде перехоплений, PHP видасть фатальну помилку: "`Uncaught Exception ...`(Неперехоплений виняток), якщо не був визначений обробник помилок за допомогою функції [setexceptionhandler()](function.set-exception-handler.html)

Починаючи з PHP 7.1.0 блок [`catch`](language.exceptions.html#language.exceptions.catch) може приймати кілька типів винятків за допомогою символу (`|`). Це корисно, коли різні винятки із різних ієрархій класів обробляються однаково.

Починаючи з PHP 8.0.0, завдання змінної для спійманого виключення є опціональним. Якщо вона не задана, блок [`catch`](language.exceptions.html#language.exceptions.catch) буде виконуватися, але не матиме доступу до об'єкта виключення.

### `finally`

Блок [`finally`](language.exceptions.html#language.exceptions.finally) також можна використовувати після або замість блоку [`catch`](language.exceptions.html#language.exceptions.catch). Код у блоці [`finally`](language.exceptions.html#language.exceptions.finally) завжди виконуватиметься після коду в блоках [`try`](language.exceptions.html) і [`catch`](language.exceptions.html#language.exceptions.catch)незалежно від того, чи було викинуто виняток, перед тим як продовжиться нормальне виконання коду.

Одна важлива взаємодія відбувається між блоком [`finally`](language.exceptions.html#language.exceptions.finally) та оператором [`return`](function.return.html). Якщо оператор [`return`](function.return.html) зустрічається усередині блоків [`try`](language.exceptions.html) або [`catch`](language.exceptions.html#language.exceptions.catch), блок [`finally`](language.exceptions.html#language.exceptions.finally) все одно буде виконано. Крім того, оператор [`return`](function.return.html) виконується, коли зустрічається, але результат буде повернутий після виконання блоку [`finally`](language.exceptions.html#language.exceptions.finally). Якщо блок [`finally`](language.exceptions.html#language.exceptions.finally) також містить оператор [`return`](function.return.html), повертається значення, вказане у блоці [`finally`](language.exceptions.html#language.exceptions.finally)

### `Глобальный обработчик исключений`

Якщо виняток дійшов стеку викликів до глобальної області видимості, може бути оброблено глобальним обробником винятків, якщо він заданий. За допомогою функції [setexceptionhandler()](function.set-exception-handler.html) можна встановити функцію, яка буде виконана замість блоку [`catch`](language.exceptions.html#language.exceptions.catch)якщо не знайшлося відповідного. Ефект аналогічний тому, ніби ми всю нашу програму обернули на блок. [`try`](language.exceptions.html)[`catch`](language.exceptions.html#language.exceptions.catch), де за реалізацію блоку [`catch`](language.exceptions.html#language.exceptions.catch) відповідає встановлена ​​функція.

### Примітки

> **Зауваження**
> 
> Внутрішні функції PHP переважно використовують [повідомлення про помилки](errorfunc.configuration.html#ini.error-reporting), і тільки нові [об'єктно-орієнтовані](language.oop5.html) модулі використовують винятки. Однак, помилки можна легко перетворити на винятки за допомогою класу [ErrorException](class.errorexception.html). Однак це не спрацює для фатальних помилок.
> 
> **Приклад #3 Перетворення повідомлення про помилки на виключення**
> 
> ```php
> <?php
> function exceptions_error_handler($severity, $message, $filename, $lineno) {
>     throw new ErrorException($message, 0, $severity, $filename, $lineno);
> }
> 
> set_error_handler('exceptions_error_handler');
> ?>
> ```

**Підказка**

[Стандартная библиотека PHP (SPL)](intro.spl.html) надає гарний набір [вбудованих класів винятків](spl.exceptions.html)

### Приклади

**Приклад #4 Викидання винятків**

```php
<?php
function inverse($x) {
    if (!$x) {
        throw new Exception('Деление на ноль.');
    }
    return 1/$x;
}

try {
    echo inverse(5) . "\n";
    echo inverse(0) . "\n";
} catch (Exception $e) {
    echo 'Выброшено исключение: ',  $e->getMessage(), "\n";
}

// Продолжение выполнения
echo "Привет, мир\n";
?>
```

Результат виконання цього прикладу:

```
0.2
Выброшено исключение: Деление на ноль.
Привет, мир
```

**Приклад #5 Обробка виключень за допомогою блоку [`finally`](language.exceptions.html#language.exceptions.finally)**

```php
<?php
function inverse($x) {
    if (!$x) {
        throw new Exception('Деление на ноль.');
    }
    return 1/$x;
}

try {
    echo inverse(5) . "\n";
} catch (Exception $e) {
    echo 'Поймано исключение: ',  $e->getMessage(), "\n";
} finally {
    echo "Первый блок finally.\n";
}

try {
    echo inverse(0) . "\n";
} catch (Exception $e) {
    echo 'Поймано исключение: ',  $e->getMessage(), "\n";
} finally {
    echo "Второй блок finally.\n";
}

// Продолжение нормального выполнения
echo "Привет, мир\n";
?>
```

Результат виконання цього прикладу:

```
0.2
Первый блок finally.
Поймано исключение: Деление на ноль.
Второй блок finally.
Привет, мир
```

**Приклад #6 Взаємодія між блоками [`finally`](language.exceptions.html#language.exceptions.finally) і [`return`](function.return.html)**

```php
<?php

function test() {
    try {
        throw new Exception('foo');
    } catch (Exception $e) {
        return 'catch';
    } finally {
        return 'finally';
    }
}

echo test();
?>
```

Результат виконання цього прикладу:

```
finally
```

**Приклад #7 Вкладені винятки**

```php
<?php

class MyException extends Exception { }

class Test {
    public function testing() {
        try {
            try {
                throw new MyException('foo!');
            } catch (MyException $e) {
                // повторный выброс исключения
                throw $e;
            }
        } catch (Exception $e) {
            var_dump($e->getMessage());
        }
    }
}

$foo = new Test;
$foo->testing();

?>
```

Результат виконання цього прикладу:

```
string(4) "foo!"
```

**Приклад #8 Обробка кількох винятків в одному блоці catch**

```php
<?php

class MyException extends Exception { }

class MyOtherException extends Exception { }

class Test {
    public function testing() {
        try {
            throw new MyException();
        } catch (MyException | MyOtherException $e) {
            var_dump(get_class($e));
        }
    }
}

$foo = new Test;
$foo->testing();

?>
```

Результат виконання цього прикладу:

```
string(11) "MyException"
```

**Приклад #9 Приклад блоку [`catch`](language.exceptions.html#language.exceptions.catch) без вказівки змінної**

Допустимо починаючи з PHP 8.0.0

```php
<?php

class SpecificException extends Exception {}

function test() {
    throw new SpecificException('Ой!');
}

try {
    test();
} catch (SpecificException) {
    print "Было поймано исключение SpecificException, но нам безразлично, что у него внутри.";
}
?>
```

**Приклад #10 Throw як вираз**

Допустимо починаючи з PHP 8.0.0

```php
<?php

class SpecificException extends Exception {}

function test() {
    do_something_risky() or throw new Exception('Всё сломалось');
}

try {
    test();
} catch (Exception $e) {
    print $e->getMessage();
}
?>
```