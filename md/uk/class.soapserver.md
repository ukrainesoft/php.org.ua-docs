Клас SoapServer

-   [« SoapClient::soapCall](soapclient.soapcall.html)
    
-   [SoapServer::addFunction »](soapserver.addfunction.html)
    
-   [PHP Manual](index.html)
    
-   [SOAP](book.soap.html)
    
-   Клас SoapServer
    

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
     resource
      $service;

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

soapfault

## Зміст

-   [SoapServer::addFunction](soapserver.addfunction.html) — Додає одну або кілька функцій обробки запитів SOAP
-   [SoapServer::addSoapHeader](soapserver.addsoapheader.html) — Додати заголовок SOAP у відповідь
-   [SoapServer::construct](soapserver.construct.html) - Конструктор SoapServer
-   [SoapServer::fault](soapserver.fault.html) — Вимушує SoapServer повернути помилку
-   [SoapServer::getFunctions](soapserver.getfunctions.html) — Повернути список функцій
-   [SoapServer::handle](soapserver.handle.html) - Обробка SOAP-запиту
-   [SoapServer::setClass](soapserver.setclass.html) - Встановлює клас, який обробляє SOAP-запити
-   [SoapServer::setObject](soapserver.setobject.html) — Встановлює об'єкт, який використовуватиметься для обробки SOAP-запитів
-   [SoapServer::setPersistence](soapserver.setpersistence.html) — Встановлює режим збереження SoapServer