Встановити, чи слід використовувати обробник помилок SOAP

-   [« is\_soap\_fault](function.is-soap-fault.html)
    
-   [SoapClient »](class.soapclient.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SOAP](ref.soap.html)
    
-   Встановити, чи слід використовувати обробник помилок SOAP
    

# usesoaperrorhandler

(PHP 5, PHP 7, PHP 8)

usesoaperrorhandler — Визначте, чи потрібно використовувати обробник помилок SOAP.

### Опис

```methodsynopsis
use_soap_error_handler(bool $enable = true): bool
```

Ця функція визначає, чи потрібно використовувати обробники помилок SOAP у сервері SOAP. Функція повертає попереднє значення. Якщо встановлено **`true`**, то подробиці помилок у додатку з класом [SoapServer](class.soapserver.html) будуть надіслані клієнту як повідомлення про помилку SOAP. Якщо встановлено **`false`**, то використовується стандартний обробник помилок PHP. За замовчуванням використовується надсилання повідомлення про помилку клієнта SOAP.

### Список параметрів

`enable`

Для надсилання даних про помилки клієнтам необхідно встановити **`true`**

### Значення, що повертаються

Повертає попереднє значення.

### Дивіться також

-   [set\_error\_handler()](function.set-error-handler.html) - Задає користувальницький обробник помилок
-   [set\_exception\_handler()](function.set-exception-handler.html) - Задає користувальницький обробник винятків