Встановлює cookie для запитів SOAP

-   [« SoapClient::getTypes](soapclient.gettypes.html)
    
-   [SoapClient::setLocation »](soapclient.setlocation.html)
    
-   [PHP Manual](index.html)
    
-   [SoapClient](class.soapclient.html)
    
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
> Виклик цього методу вплине на всі наступні виклики методів [SoapClient](class.soapclient.html)

### Список параметрів

`name`

Ім'я cookie.

`value`

Значення cookie. Якщо не вказано, cookie буде видалено.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание                              |
|--------|---------------------------------------|
|        | `value` тепер допускає значення null. |