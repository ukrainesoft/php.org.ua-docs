---
navigation:
  - function.is-soap-fault.md: « is\_soap\_fault
  - class.soapclient.md: SoapClient »
  - index.md: PHP Manual
  - ref.soap.md: Функції SOAP
title: use\_soap\_error\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# use\_soap\_error\_handler

(PHP 5, PHP 7, PHP 8)

use\_soap\_error\_handler — Визначте, чи потрібно використовувати обробник помилок SOAP.

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

-   [set\_error\_handler()](function.set-error-handler.md) \- Задає користувальницький обробник помилок
-   [set\_exception\_handler()](function.set-exception-handler.md) \- Задає користувальницький обробник винятків
