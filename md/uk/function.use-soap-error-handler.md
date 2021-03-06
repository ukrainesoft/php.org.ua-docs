- [«is_soap_fault](function.is-soap-fault.md)
- [SoapClient »](class.soapclient.md)

- [PHP Manual](index.md)
- [Функції SOAP](ref.soap.md)
- Встановити, чи слід використовувати обробник помилок SOAP

#use_soap_error_handler

(PHP 5, PHP 7, PHP 8)

use_soap_error_handler — Встановити, чи потрібно використовувати обробник
помилок SOAP

### Опис

**use_soap_error_handler**(bool `$enable` = **`true`**): bool

Ця функція визначає, чи потрібно використовувати обробники помилок SOAP
SOAP-сервер. Функція повертає попереднє значення. Якщо встановлено
**`true`**, то подробиці помилок у додатку з класом
[SoapServer](class.soapserver.md) буде відправлено клієнту як
повідомлення про помилку SOAP. Якщо встановлено в **`false`**, то
використовується стандартний обробник помилок PHP. За замовчуванням
використовується надсилання повідомлення про помилку SOAP клієнта.

### Список параметрів

`enable`
Для надсилання даних про помилки клієнтам необхідно встановити
**`true`**.

### Значення, що повертаються

Повертає попереднє значення.

### Дивіться також

- [set_error_handler()](function.set-error-handler.md) - Задає
користувальницький обробник помилок
- [set_exception_handler()](function.set-exception-handler.md) -
Задає користувальницький обробник винятків
