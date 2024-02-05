---
navigation:
  - intlchar.toupper.md: '« IntlChar::toupper'
  - class.intliterator.md: IntlIterator »
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас винятків для помилок intl
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас винятків для помилок intl

(PHP 5 > 5.5.0, PHP 7, PHP 8, PECL intl > 3.0.0a1)

## Вступ

Цей клас служить для виклику винятків у разі помилки у функціях intl. Ці винятки можуть бути викинуті лише якщо включена опція [intl.use\_exceptions](intl.configuration.md#ini.intl.use-exceptions)

## Огляд класів

```classsynopsis

    
     class IntlException
    

    
     extends
      Exception
     {

    /* Наследуемые свойства */
    
      protected
      string
       $message = "";
private
      string
       $string = "";
protected
      int
       $code;
protected
      string
       $file = "";
protected
      int
       $line;
private
      array
       $trace = [];
private
      ?Throwable
       $previous = null;


    /* Наследуемые методы */
    
   public Exception::__construct(string $message = "", int $code = 0, ?Throwable $previous = null)

    final public Exception::getMessage(): string
final public Exception::getPrevious(): ?Throwable
final public Exception::getCode(): int
final public Exception::getFile(): string
final public Exception::getLine(): int
final public Exception::getTrace(): array
final public Exception::getTraceAsString(): string
public Exception::__toString(): string
private Exception::__clone(): void

   }
```
