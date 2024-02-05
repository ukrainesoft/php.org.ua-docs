---
navigation:
  - soapclient.soapcall.md: '« SoapClient::\_\_soapCall'
  - soapserver.addfunction.md: 'SoapServer::addFunction »'
  - index.md: PHP Manual
  - book.soap.md: SOAP
title: Клас SoapServer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SoapServer

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас SoapServer є сервером для протоколів [» SOAP 1.1](http://www.w3.org/TR/soap11/) і [» SOAP 1.2](http://www.w3.org/TR/soap12/). Його можна використовувати з описом служби WSDL або без нього.

## Огляд класів

```classsynopsis

    
     class SoapServer
     {

    /* Свойства */
    
     private
     ?SoapFault
      $__soap_fault = null;


    /* Методы */
    
   public __construct(?string $wsdl, array $options = [])

    public addFunction(array|string|int $functions): void
public addSoapHeader(SoapHeader $header): void
public fault(    string $code,    string $string,    string $actor = "",    mixed $details = null,    string $name = ""): void
public getFunctions(): array
public handle(?string $request = null): void
public setClass(string $class, mixed ...$args): void
public setObject(object $object): void
public setPersistence(int $mode): void

   }
```

## Властивості

service

\_\_soap\_fault

## Зміст

-   [SoapServer::addFunction](soapserver.addfunction.md)— Додає одну або кілька функцій обробки запитів SOAP
-   [SoapServer::addSoapHeader](soapserver.addsoapheader.md)— Додати заголовок SOAP у відповідь
-   [SoapServer::\_\_construct](soapserver.construct.md) \- Конструктор SoapServer
-   [SoapServer::fault](soapserver.fault.md) \- Примушує SoapServer повернути помилку
-   [SoapServer::getFunctions](soapserver.getfunctions.md)— Повернути список функцій
-   [SoapServer::handle](soapserver.handle.md) \- Обробка SOAP-запиту
-   [SoapServer::setClass](soapserver.setclass.md) \- Встановлює клас, який обробляє SOAP-запити
-   [SoapServer::setObject](soapserver.setobject.md)— Встановлює об'єкт, який використовуватиметься для обробки SOAP-запитів
-   [SoapServer::setPersistence](soapserver.setpersistence.md)— Встановлює режим збереження SoapServer
