---
navigation:
  - class.mongodb-driver-exception-logicexception.md: « MongoDB\\Driver\\Exception\\LogicException
  - mongodb-driver-runtimeexception.haserrorlabel.md: 'MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel »'
  - index.md: PHP Manual
  - mongodb.exceptions.md: MongoDB\\Driver\\Exception
title: Клас MongoDB\\Driver\\Exception\\RuntimeException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Exception\\RuntimeException

(mongodb >= 1.0.0)

## Вступ

Викидається, коли драйвер виявляє помилку під час виконання (наприклад, внутрішня помилка з [» libmongoc](https://github.com/mongodb/mongo-c-driver)

## Огляд класів

```classsynopsis



    
     
      class MongoDB\Driver\Exception\RuntimeException
     

     
      extends
       RuntimeException
     

     implements 
       MongoDB\Driver\Exception\Exception {

    /* Свойства */
    
     protected
     ?array
      $errorLabels;


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
    
   final public hasErrorLabel(string $errorLabel): bool


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

errorLabels

Містить масив позначок помилок для виключення. Наприклад, мітки помилок можуть використовуватися для визначення того, чи можна безпечно провести транзакцію, якщо є мітка TransientTransactionError. Існування певної мітки помилки має бути перевірено за допомогою [MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel()](mongodb-driver-runtimeexception.haserrorlabel.md) замість інтерпретації цієї властивості errorlabels вручну.

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.6.0 |  |
| Доданий метод [MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel()](mongodb-driver-runtimeexception.haserrorlabel.md) і властивість [MongoDB\\Driver\\Exception\\RuntimeException::errorLabels](class.mongodb-driver-exception-runtimeexception.md#mongodb-driver-exception-runtimeexception.props.errorlabels) |  |

## Зміст

-   [MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel](mongodb-driver-runtimeexception.haserrorlabel.md)— Повертає, чи мітка помилки пов'язана з винятком
