---
navigation:
  - function.is-soap-fault.html: « issoapfault
  - class.soapclient.html: SoapClient »
  - index.html: PHP Manual
  - ref.soap.html: Функции SOAP
title: usesoaperrorhandler
---
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

-   [seterrorhandler()](function.set-error-handler.html) - Задає користувальницький обробник помилок
-   [setexceptionhandler()](function.set-exception-handler.html) - Задає користувальницький обробник винятків
