Клас V8JsException

-   [« V8Js::registerExtension](v8js.registerextension.md)
    
-   [V8JsException::getJsFileName »](v8jsexception.getjsfilename.md)
    
-   [PHP Manual](index.md)
    
-   [V8js](book.v8js.md)
    
-   Клас V8JsException
    

# Клас [V8JsException](class.v8jsexception.md)

(PECL v8js >= 0.1.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class V8JsException
     

     
      extends
       Exception
     
     {
    
    /* Свойства */
    
     protected
      $JsFileName;

    protected
      $JsLineNumber;

    protected
      $JsSourceLine;

    protected
      $JsTrace;


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


    /* Методы */
    
   final public getJsFileName(): string
final public getJsLineNumber(): int
final public getJsSourceLine(): string
final public getJsTrace(): string


    /* Наследуемые методы */
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

## Властивості

JsFileName

JsLineNumber

JsSourceLine

JsTrace

## Зміст

-   [V8JsException::getJsFileName](v8jsexception.getjsfilename.md) — Отримати ім'я JavaScript
-   [V8JsException::getJsLineNumber](v8jsexception.getjslinenumber.md) — Отримати номер рядка
-   [V8JsException::getJsSourceLine](v8jsexception.getjssourceline.md) — Отримати вихідний рядок JavaScript
-   [V8JsException::getJsTrace](v8jsexception.getjstrace.md) — Отримати стек викликів