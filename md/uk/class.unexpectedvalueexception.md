- [« UnderflowException](class.underflowexception.md)
- [Функції SPL»](ref.spl.md)

- [PHP Manual](index.md)
- [Виключення](spl.exceptions.md)
- Клас UnexpectedValueException

# Клас UnexpectedValueException

(PHP 5 \>= 5.1.0, PHP 7, PHP 8)

## Вступ

Викидається виняток, якщо значення не співпадає з набором значень.
Зазвичай це відбувається, коли функція викликає іншу функцію і чекає,
що значення, що повертається, буде певного типу або значенням, не
включаючи арифметичні помилки або помилки, пов'язані з буфером.

## Огляд класів

class **UnexpectedValueException** extends
[RuntimeException](class.runtimeexception.md) {

/\* Наслідувані властивості \*/

protected string `$message` = "";

private string `$string` = "";

protected int `$code`;

protected string `$file` = "";

protected int `$line`;

private array `$trace` = [];
 private ?[Throwable](class.throwable.md) `$previous` = null;

/\* Наслідувані методи \*/

final public [Exception::getMessage](exception.getmessage.md)():
string

final public [Exception::getPrevious](exception.getprevious.md)():
?[Throwable](class.throwable.md)

final public [Exception::getCode](exception.getcode.md)(): int

final public [Exception::getFile](exception.getfile.md)(): string

final public [Exception::getLine](exception.getline.md)(): int

final public [Exception::getTrace](exception.gettrace.md)(): array

final public
[Exception::getTraceAsString](exception.gettraceasstring.md)(): string

public [Exception::\_\_toString](exception.tostring.md)(): string

private [Exception::\_\_clone](exception.clone.md)(): void

}
