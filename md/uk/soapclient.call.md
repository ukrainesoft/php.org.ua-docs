Викликає SOAP-функцію (застарілий метод)

-   [« SoapClient](class.soapclient.html)
    
-   [SoapClient::construct »](soapclient.construct.html)
    
-   [PHP Manual](index.html)
    
-   [SoapClient](class.soapclient.html)
    
-   Викликає SOAP-функцію (застарілий метод)
    

# SoapClient::call

(PHP 5, PHP 7, PHP 8)

SoapClient::call - Викликає SOAP-функцію (застарілий метод)

### Опис

```methodsynopsis
public SoapClient::__call(string $name, array $args): mixed
```

Виклик цього методу застарів. Зазвичай функції SOAP можуть бути викликані як методи об'єкта [SoapClient](class.soapclient.html); у ситуаціях, коли це неможливо або потрібні додаткові опції, використовуйте метод [SoapClient::soapCall()](soapclient.soapcall.html)

### Список параметрів

`name`

Ім'я функції SOAP.

`args`

Масив аргументів передачі функції. Може бути впорядкований чи асоціативний масив. Зверніть увагу, що більшість серверів SOAP вимагають надання імен параметрів, у цьому випадку має бути асоціативний масив.

### Значення, що повертаються

Функції SOAP можуть повертати одне чи кілька значень. Якщо функція SOAP повертає лише одне значення, то значення, що повертається, буде скаляром. Якщо повертається кілька значень, замість них повертається асоціативний масив іменованих вихідних параметрів.

У разі виникнення помилки, якщо об'єкт [SoapClient](class.soapclient.html) був оголошений з опцією `exceptions` зі значенням **`false`**, буде повернуто об'єкт [SoapFault](class.soapfault.html)