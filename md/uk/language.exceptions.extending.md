---
navigation:
  - language.exceptions.md: « Винятки
  - language.fibers.md: Fibers »
  - index.md: PHP Manual
  - language.exceptions.md: Винятки
title: Спадкування винятків
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Спадкування винятків

Визначений користувачем клас виключення повинен бути визначений як клас розширювальний (успадкований) вбудований клас Exception. Нижче наведено методи та властивості класу Exception, доступні дочірнім класам.

**Приклад #1 Вбудований клас Exception**

```php
<?php
class Exception implements Throwable
{
    protected $message = 'Unknown exception';   // сообщение об исключении
    private   $string;                          // свойство для __toString
    protected $code = 0;                        // пользовательский код исключения
    protected $file;                            // файл, в котором было выброшено исключение
    protected $line;                            // строка, в которой было выброшено исключение
    private   $trace;                           // трассировка вызовов методов и функций
    private   $previous;                        // предыдущее исключение, если исключение вложенное

    public function __construct($message = '', $code = 0, Throwable $previous = null);

    final private function __clone();           // запрещает клонирования исключения

    final public  function getMessage();        // сообщение исключения
    final public  function getCode();           // код исключения
    final public  function getFile();           // файл, где выброшено исключение
    final public  function getLine();           // строка, на которой выброшено исключение
    final public  function getTrace();          // массив backtrace()
    final public  function getPrevious();       // предыдущее исключение
    final public  function getTraceAsString();  // отформатированная строка трассировки

    // Переопределяемый
    public function __toString();               // отформатированная строка для отображения
}
?>
```

Якщо клас, успадкований від Exception перевизначає [конструктор](language.oop5.decon.md)необхідно викликати в конструкторі [parent::\_\_construct()](language.oop5.paamayim-nekudotayim.md)щоб бути впевненим, що всі доступні дані були правильно присвоєні. Метод [\_\_toString()](language.oop5.magic.md) може бути перевизначений, щоб забезпечити потрібний висновок, коли об'єкт перетворюється на рядок.

> **Зауваження** :
> 
> Винятки не можна клонувати. Спроба [клонувати](language.oop5.cloning.md) виняток призведе до непоправної помилки **`E_ERROR`**

**Приклад #2 Спадкування класу Exception**

```php
<?php
/**
 * Определим свой класс исключения
 */
class MyException extends Exception
{
    // Переопределим исключение так, что параметр message станет обязательным
    public function __construct($message, $code = 0, Throwable $previous = null) {
        // некоторый код

        // убедитесь, что все передаваемые параметры верны
        parent::__construct($message, $code, $previous);
    }

    // Переопределим строковое представление объекта.
    public function __toString() {
        return __CLASS__ . ": [{$this->code}]: {$this->message}\n";
    }

    public function customFunction() {
        echo "Мы можем определять новые методы в наследуемом классе\n";
    }
}


/**
 * Создадим класс для тестирования исключения
 */
class TestException
{
    public $var;

    const THROW_NONE    = 0;
    const THROW_CUSTOM  = 1;
    const THROW_DEFAULT = 2;

    function __construct($avalue = self::THROW_NONE) {

        switch ($avalue) {
            case self::THROW_CUSTOM:
                // Выбрасываем собственное исключение
                throw new MyException('1 - неправильный параметр', 5);
                break;

            case self::THROW_DEFAULT:
                // Выбрасываем встроеное исключение
                throw new Exception('2 - недопустимый параметр', 6);
                break;

            default:
                // Никаких исключений, объект будет создан.
                $this->var = $avalue;
                break;
        }
    }
}

// Пример 1
try {
    $o = new TestException(TestException::THROW_CUSTOM);
} catch (MyException $e) {      // Будет перехвачено
    echo "Поймано собственное переопределённое исключение\n", $e;
    $e->customFunction();
} catch (Exception $e) {        // Будет пропущено
    echo "Поймано встроенное исключение\n", $e;
}

// Отсюда будет продолжено выполнение программы
var_dump($o); // Null
echo "\n\n";


// Пример 2
try {
    $o = new TestException(TestException::THROW_DEFAULT);
} catch (MyException $e) {      // Тип исключения не совпадёт
    echo "Поймано переопределённое исключение\n", $e;
    $e->customFunction();
} catch (Exception $e) {        // Будет перехвачено
    echo "Перехвачено встроенное исключение\n", $e;
}

// Отсюда будет продолжено выполнение программы
var_dump($o); // Null
echo "\n\n";


// Пример 3
try {
    $o = new TestException(TestException::THROW_CUSTOM);
} catch (Exception $e) {        // Будет перехвачено
    echo "Поймано встроенное исключение\n", $e;
}

// Продолжение исполнения программы
var_dump($o); // Null
echo "\n\n";


// Пример 4
try {
    $o = new TestException();
} catch (Exception $e) {        // Будет пропущено, т.к. исключение не выбрасывается
    echo "Поймано встроенное исключение\n", $e;
}

// Продолжение выполнения программы
var_dump($o); // TestException
echo "\n\n";
?>
```
