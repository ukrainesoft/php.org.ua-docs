---
navigation:
  - function.is-soap-fault.md: « issoapfault
  - class.soapclient.md: SoapClient »
  - index.md: PHP Manual
  - ref.soap.md: Функции SOAP
title: usesoaperrorhandler
---
# usesoaperrorhandler

(PHP 5, PHP 7, PHP 8)

usesoaperrorhandler — Визначте, чи потрібно використовувати обробник помилок SOAP.

### Опис

```methodsynopsis
use_soap_error_handler(bool $enable = true): bool
```

Ця функція визначає, чи потрібно використовувати обробники помилок SOAP у сервері SOAP. Функція повертає попереднє значення. Якщо встановлено **`true`**, то подробиці помилок у додатку з класом [SoapServer](class.soapserver.md) будуть надіслані клієнту як повідомлення про помилку SOAP. Якщо встановлено **`false`**, то використовується стандартний обробник помилок PHP. За замовчуванням використовується надсилання повідомлення про помилку клієнта SOAP.

### Список параметрів

`enable`

Для надсилання даних про помилки клієнтам необхідно встановити **`true`**

### Значення, що повертаються

Повертає попереднє значення.

### Дивіться також

-   [seterrorhandler()](function.set-error-handler.md) - Задає користувальницький обробник помилок
-   [setexceptionhandler()](function.set-exception-handler.md) - Задає користувальницький обробник винятків
