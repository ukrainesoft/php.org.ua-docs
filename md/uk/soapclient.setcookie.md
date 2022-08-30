Встановлює cookie для запитів SOAP

-   [« SoapClient::getTypes](soapclient.gettypes.md)
    
-   [SoapClient::setLocation »](soapclient.setlocation.md)
    
-   [PHP Manual](index.md)
    
-   [SoapClient](class.soapclient.md)
    
-   Встановлює cookie для запитів SOAP
    

# SoapClient::setCookie

(PHP 5> = 5.0.4, PHP 7, PHP 8)

SoapClient::setCookie — Встановлює cookie для запитів SOAP

### Опис

```methodsynopsis
public SoapClient::__setCookie(string $name, ?string $value = null): void
```

Визначає cookie, які будуть надіслані із SOAP-запитами.

> **Зауваження**
> 
> Виклик цього методу вплине на всі наступні виклики методів [SoapClient](class.soapclient.md)

### Список параметрів

`name`

Ім'я cookie.

`value`

Значення cookie. Якщо не вказано, cookie буде видалено.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `value` тепер допускає значення null. |