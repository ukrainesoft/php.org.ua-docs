---
navigation:
  - oauthprovider.tokenhandler.md: '« OAuthProvider::tokenHandler'
  - book.soap.md: SOAP »
  - index.md: PHP Manual
  - book.oauth.md: OAuth
title: Клас OAuthException
---
# Клас OAuthException

(PECL OAuth >= 0.99.1)

## Вступ

Це виняток викидається у разі виникнення помилок під час використання модуля OAuth і містить корисну налагоджувальну інформацію.

## Огляд класів

```classsynopsis


    
    
     
      class OAuthException
     

     
      extends
       Exception
     
     {
    
    /* Свойства */
    
     public
      $lastResponse;

    public
      $debugInfo;


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

lastResponse

Останній виняток, якщо такий є

debugInfo
